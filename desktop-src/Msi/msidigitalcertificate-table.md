---
description: В таблице Мсидигиталцертификате хранятся сертификаты в двоичном формате потока и каждый сертификат связывается с первичным ключом.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Таблица Мсидигиталцертификате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443e5f27d13ebd823fa8e5362de474082d39e4b09b9e240b9ee16e9924342e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828784"
---
# <a name="msidigitalcertificate-table"></a>Таблица Мсидигиталцертификате

В таблице Мсидигиталцертификате хранятся сертификаты в двоичном формате потока и каждый сертификат связывается с первичным ключом. Первичный ключ используется для обмена сертификатами между несколькими объектами с цифровой подписью. Цифровой сертификат — это учетные данные, которые предоставляют средства для проверки удостоверения. дополнительные сведения см. в статье [цифровые сертификаты](../seccrypto/digital-certificates.md) в разделе [криптография](../seccrypto/cryptography-portal.md) Microsoft Windows Software Development Kit (SDK).

таблицы [мсидигиталсигнатуре](msidigitalsignature-table.md) и мсидигиталцертификате доступны начиная с установщик Windows версии 2,0.

Windows Установщик может использовать цифровые подписи в качестве средства для обнаружения поврежденных ресурсов. Windows Установщик версии 2,0 может проверять только цифровые подписи внешних ящиков и только с помощью таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md) и мсидигиталцертификате.

начиная с версии установщик Windows 3,0, установщик Windows может проверять цифровые подписи исправлений (msp-файлы) с помощью таблиц [мсипатчцертификате](msipatchcertificate-table.md) и мсидигиталцертификате. Дополнительные сведения см. в разделе [рекомендации по разработке безопасных установок](guidelines-for-authoring-secure-installations.md) и [исправления контроля учетных записей (UAC)](user-account-control--uac--patching.md).

Таблица Мсидигиталцертификате содержит следующие столбцы.



| Столбец             | Type                         | Ключ | Допускает значения NULL |
|--------------------|------------------------------|-----|----------|
| дигиталцертификате | [Идентификатор](identifier.md) | Д   | Нет        |
| цертдата           | [Двоичный](binary.md)         | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>дигиталцертификате
</dt> <dd>

Идентифицирует сертификат цифровой подписи. Первичный ключ таблицы.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>цертдата
</dt> <dd>

Двоичное представление цифрового сертификата. Столбец Цертдата содержит закодированный байтовый массив контекста сертификата. Это элемент **пбцертенкодед** структуры [**\_ контекста CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) . Контекст сертификата можно получить, вызвав [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)или импортировав CER-файл.

</dd> </dl>

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Таблица Мсидигиталсигнатуре](msidigitalsignature-table.md)
</dt> <dt>

[цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
