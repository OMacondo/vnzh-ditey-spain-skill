# Подача через Mercurio

**Адреса:** https://mercurio.delegaciondelgobierno.gob.es/mercurio (стара адреса на sede.administracionespublicas.gob.es перенаправляє сюди).

- ✅ **Вхід** того з батьків, хто подає, своїм сертифікатом. Вхід іде через шлюз Cl@ve. ⚠ Вхід через Cl@ve PIN/Permanente не перевіряли.
- ✅ **Підпис** сертифікатом через AutoFirma, на Mac у Chrome (див. `sertyfikat-autofirma.md`). ✅ (друга родина) На Windows у Chrome теж спрацював.
- Кожна дитина подається **окремою заявою**.
- Вимкни автоматичний переклад сторінки (Google Translate): він може ламати кнопки й форми.
- Заява подається з території Іспанії: на момент подачі і той, хто подає, і дитина мають бути в Іспанії (так було в нас).

## Підготовка файлів (`Подача_Mercurio/`)
✅ Обмеження, як вони були на екрані завантаження:
- **≤ 6 МБ** на файл (PDF);
- ✅ (друга родина) **≤ 15 МБ разом** на одну заяву. Ліміт впирається швидко, бо документи батьків ідуть у кожну заяву. Стисни скани паспортів і TIE заздалегідь (наприклад, ~110–150 dpi) і порахуй суму по кожній дитині;
- у назвах лише латиниця, цифри, «_» і «-»;
- **один файл на кожен обов'язковий тип документа**. Якщо документів кілька (наприклад, квитанція і бланк мита), об'єднай їх в один PDF. Тип «Otros documentos» можна вибирати кілька разів, щоразу з текстовим описом.

Ще одна порада, яку ми не перевіряли: PDF не має бути захищений паролем.

Mercurio може відхилити файл, не пояснивши причини. У нас так сталося один раз, з PDF, склеєним зі сканів зі сторінками різного розміру. Допомогло перезібрати файл наново з однаковими сторінками. Можливо, це був поодинокий випадок.

Рекомендовані назви:
```
01_Certificado_nacimiento_<ДИТИНА>_original_apostilla_traduccion.pdf
02_Padron_familiar.pdf
03_Certificado_escolar_<ДИТИНА>.pdf          (6–16 років)
03b_Declaracion_escolarizacion.pdf           (бланк декларації, див. dokumenty.md)
04_Pasaporte_TIE_<ХТО_ПОДАЄ>.pdf
04_Pasaporte_TIE_<ДРУГИЙ_З_БАТЬКІВ>.pdf
05_Pasaporte_TIE_<ДИТИНА>.pdf
07_Apoderamiento_<ДРУГИЙ>_a_<ХТО_ПОДАЄ>.pdf
09_Tasa_790-052_<ДИТИНА>_completo.pdf        (квитанція з NRC + бланк)
```

Якщо файл перевищує 6 МБ, стисни зображення (наприклад, JPEG ~150 dpi), **зберігаючи розмір сторінок**. Після цього перевір, що текст читається.

## ✅ Кроки в Mercurio (так було в жовтні 2026)
1. Вхід → на головній, праворуч, розділ «Presentar solicitud o aportar documentos a expedientes» → **CONTINUAR PRESENTACIÓN**. Ліва кнопка, «Consulta de solicitud existente», потрібна для перевірки статусу.
2. «Solicitudes permitidas en la provincia de …»: перевір провінцію → ◉ **EX25** → CONTINUAR. Не вибирай EX26 («modificación»), хоча процес і називають «модифікацією».
3. **Тип дозволу:** блок «RESIDENCIA MENOR EXTRANJERO ACOMPAÑADO (CAP I)» → ◉ **art. 160**. Галочку «NO CONSIENTO» не став → CONTINUAR.
4. Вкладка **DATOS DEL SOLICITANTE** (дитина й представник), див. `ex25.md` → CONTINUAR.
5. Вкладка **DOMICILIO DE NOTIFICACIÓN**: «Domicilio del solicitante» → виправ ім'я та NIE на того, хто подає → ☑ **Consiento** → **CONCLUIR**.
6. Вікно про захист персональних даних (RGPD) → Aceptar.
7. Екран з **«Id formulario inicial»**, тобто номером заяви. Запиши його.
   - **DESCARGAR SOLICITUD**: за бажанням, PDF заяви для себе.
   - **PRESENTACIÓN ELECTRÓNICA**: перехід далі.
8. **Confirmación de sujeto legitimado:** ☑ *DECLARO bajo mi responsabilidad … que soy el sujeto legitimado para presentar esta solicitud y me encuentro en territorio español* → Aceptar.
9. **Документи:** для кожного файлу *Examinar…* → вибрати тип у **Descripción** → **ADJUNTAR DOCUMENTO**.

| Файл | Тип (Descripción) |
|---|---|
| 05_Pasaporte_TIE_<ДИТИНА> | *Pasaporte, título de viaje o cédula de inscripción completos, válidos y en vigor del menor* |
| 04_Pasaporte_TIE_<ХТО_ПОДАЄ> | *Acreditación de la identidad del representante legal (DNI o pasaporte completo)* |
| 01_Certificado_nacimiento_… | *Acreditación de la representación legal del menor (certificado de nacimiento o tutela)* |
| 03_Certificado_escolar_… | *En su caso, informe sobre escolarización de menores a cargo en España* |
| 09_Tasa_…_completo | *Tasa (mod. 790 cód. 052)* |
| 02_Padron_familiar | *Otros documentos que desee aportar* → опис: CERTIFICADO DE EMPADRONAMIENTO FAMILIAR |
| 04_Pasaporte_TIE_<ДРУГИЙ> | *Otros documentos* → PASAPORTE Y TIE DEL PADRE / DE LA MADRE |
| 07_Apoderamiento_… | *Otros documentos* → APODERAMIENTO DEL PADRE A FAVOR DE LA MADRE (або навпаки) |
| 03b_Declaracion_escolarizacion | ✅ (друга родина) *Otros documentos* → DECLARACIÓN DE ESCOLARIZACIÓN DE MENORES A CARGO |
| Письмова згода замість Apodera | ✅ (друга родина) *Otros documentos* → CONSENTIMIENTO DE LA MADRE / DEL PADRE |

   - Для «Otros documentos» Mercurio просить **текстовий опис**. Пиши коротко, великими літерами.
   - **Не вибирай** «Informe de vivienda» і «Acreditación de la permanencia continuada (mínimo 2 años)»: за SEM 2/2026 вони не потрібні.
   - Порядок завантаження не важливий. Важливо, щоб кожен файл мав правильний тип і щоб усі файли з'явилися в «Documentos adjuntados». Попроси скриншот цього списку і звір його.
   - Свій PDF з EX-25 сюди не завантажуй: заяву Mercurio вже сформував сам.

10. **CONTINUAR** → підсумок → **Firmar y Registrar** → AutoFirma → сертифікат того, хто подає.
   **Не закривай вікно**, поки не з'явиться «Su solicitud ha sido aceptada y registrada de forma correcta». Якщо вікно закрилося до підпису, заява **не подана**: почни заново, а стара чернетка просто не використовуватиметься (у нас так було з першою спробою).
11. Збережи:
    - **DESCARGAR RESGUARDO** → `10_Resguardo_<ДИТИНА>.pdf`. Це **офіційне підтвердження** з *Número de registro* (REGAGE…) і *Nº Expediente*;
    - **DESCARGAR PRESENTACIÓN** → `10_Copia_solicitud_<ДИТИНА>.pdf`. Це копія для себе.

Наступна дитина: VOLVER → CONTINUAR PRESENTACIÓN → і знову з кроку 2.

## Перевірка resguardo (зроби за користувача)
Відкрий PDF і перевір:
- ім'я та NIE дитини;
- тип EX25;
- *Número de registro*;
- *Nº Expediente*;
- орган (Oficina de Extranjería провінції);
- **кількість і назви файлів**, вони мають відповідати списку.

Запиши номери в `СТАТУС.md`.
