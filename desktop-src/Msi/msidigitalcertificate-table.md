---
description: В таблице Мсидигиталцертификате хранятся сертификаты в двоичном формате потока и каждый сертификат связывается с первичным ключом.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Таблица Мсидигиталцертификате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812712"
---
# <a name="msidigitalcertificate-table"></a>Таблица Мсидигиталцертификате

В таблице Мсидигиталцертификате хранятся сертификаты в двоичном формате потока и каждый сертификат связывается с первичным ключом. Первичный ключ используется для обмена сертификатами между несколькими объектами с цифровой подписью. Цифровой сертификат — это учетные данные, которые предоставляют средства для проверки удостоверения. Дополнительные сведения см. в статье [цифровые сертификаты](../seccrypto/digital-certificates.md) в разделе [Криптография](../seccrypto/cryptography-portal.md) пакета средств разработки программного обеспечения Microsoft Windows (SDK).

Таблицы [мсидигиталсигнатуре](msidigitalsignature-table.md) и мсидигиталцертификате доступны начиная с установщик Windows версии 2,0.

Установщик Windows могут использовать цифровые подписи в качестве средства для обнаружения поврежденных ресурсов. Установщик Windows версии 2,0 может проверять только цифровые подписи внешних ящиков и только с помощью таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md) и мсидигиталцертификате.

Начиная с версии установщик Windows 3,0, установщик Windows может проверять цифровые подписи исправлений (MSP-файлы) с помощью таблиц [мсипатчцертификате](msipatchcertificate-table.md) и мсидигиталцертификате. Дополнительные сведения см. в разделе [рекомендации по разработке безопасных установок](guidelines-for-authoring-secure-installations.md) и [исправления контроля учетных записей (UAC)](user-account-control--uac--patching.md).

Таблица Мсидигиталцертификате содержит следующие столбцы.



| Столбец             | Type                         | Ключ | Допускает значения NULL |
|--------------------|------------------------------|-----|----------|
| дигиталцертификате | [Идентификатор](identifier.md) | Да   | Нет        |
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Таблица Мсидигиталсигнатуре](msidigitalsignature-table.md)
</dt> <dt>

[Цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
