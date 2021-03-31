---
title: Создание сертификата для подписи пакета приложения
description: Узнайте, как использовать MakeCert.exe и Pvk2Pfx.exe для создания тестового сертификата подписи кода, чтобы можно было подписывать пакеты приложений Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069828"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>Создание сертификата для подписи пакета приложения

> [!IMPORTANT]
> MakeCert.exe не рекомендуется к использованию. Текущие рекомендации по созданию сертификата см. в разделе [Создание сертификата для подписания пакета](/windows/msix/package/create-certificate-package-signing).

 

Узнайте, как использовать [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) для создания тестового сертификата подписи кода, чтобы можно было подписывать пакеты приложений Windows.

Перед развертыванием пакетных приложений Windows необходимо выполнить цифровую подпись. Если вы не используете Microsoft Visual Studio 2012 для создания и подписи пакетов приложений, необходимо создать собственные сертификаты для подписи кода и управлять ими. Сертификаты можно создавать с помощью [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) из комплекта драйверов Windows (WDK). Затем можно использовать сертификаты для подписывания пакетов приложений, чтобы их можно было развернуть локально для тестирования.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Пакеты и развертывание приложений](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Средства для подписывания драйверов](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Предварительные условия

-   Средства [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) из WDK

## <a name="instructions"></a>Инструкции

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Шаг 1. Определение имени издателя пакета

Чтобы сделать сертификат подписи, который вы создадите, использовать с пакетом приложения, который необходимо подписать, имя субъекта сертификата подписи должно соответствовать атрибуту **издателя** элемента [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) в AppxManifest.xml этого приложения. Например, предположим, что AppxManifest.xml содержит:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Для параметра *publisherName* , указанного с помощью служебной программы [**MakeCert**](/windows-hardware/drivers/devtest/makecert) на следующем шаге, используйте "CN = Contoso Software, O = Contoso Corporation, C = US".

> [!Note]  
> Эта строка параметра указывается в кавычках и является учетом регистра и пробела.

 

Строка атрибута **издателя** , определенная для элемента [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) в AppxManifest.xml, должна совпадать со строкой, указанной в параметре [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n для имени субъекта сертификата. Скопируйте и вставьте строку, где это возможно.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Шаг 2. создание закрытого ключа с помощью MakeCert.exe

Используйте служебную программу [**MakeCert**](/windows-hardware/drivers/devtest/makecert) для создания самозаверяющего тестового сертификата и закрытого ключа:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Эта команда предложит указать пароль для PVK-файла. Рекомендуется выбрать [надежный пароль](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) и защитить закрытый ключ в безопасном месте.

Рекомендуется использовать предлагаемые параметры из предыдущего примера по следующим причинам.

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Создает самозаверяющий корневой сертификат. Это упрощает управление тестовым сертификатом.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Помечает базовое ограничение для сертификата как конечную сущность. Это предотвращает использование сертификата в качестве центра сертификации (ЦС), который может выдавать другие сертификаты.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/еку**
</dt> <dd>

Задает значения расширенного использования ключа (EKU) для сертификата.

> [!Note]  
> Не ставьте пробел между двумя значениями, разделенными запятыми.

 

-   1.3.6.1.5.5.7.3.3 указывает, что сертификат действителен для подписывания кода. Всегда указывайте это значение, чтобы ограничить предполагаемое использование сертификата.
-   1.3.6.1.4.1.311.10.3.13 указывает, что сертификат учитывает время существования подписи. Как правило, если подпись имеет отметку времени, при условии, что сертификат был действителен в момент времени, подпись остается действительной, даже если срок действия сертификата истек. Это расширенное EKU заставляет срок действия подписи истечь независимо от того, имеет ли подпись время отметки.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Задает дату окончания срока действия сертификата. Укажите значение параметра *expirationDate* в формате мм/дд/гггг. Рекомендуется выбирать дату истечения срока действия, если это необходимо для целей тестирования, как правило, меньше года. Эта дата окончания срока действия в сочетании с ключом времени существования подписывания может помочь ограничить окно, в котором сертификат может быть скомпрометирован и недоступен.

</dd> </dl>

Дополнительные сведения о других параметрах см. в разделе [**MakeCert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Шаг 3. Создание файла обмена личной информацией (PFX) с помощью Pvk2Pfx.exe

Используйте служебную программу [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) для преобразования файлов. PVK и. cer, созданных средством [**MakeCert**](/windows-hardware/drivers/devtest/makecert) , в PFX-файл, который можно использовать с средством [SignTool](/windows/desktop/SecCrypto/signtool) для подписания пакета приложения:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Файлы *MyKey. PVK* и *MyKey. cer* являются теми же файлами, которые [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) созданы на предыдущем шаге. С помощью необязательного параметра/по можно указать другой пароль для результирующего PFX-файла; в противном случае PFX-файл имеет тот же пароль, что и *MyKey. PVK*.

Дополнительные сведения о других параметрах см. в разделе [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Комментарии

После создания PFX-файла можно использовать файл с помощью средства [SignTool](/windows/desktop/SecCrypto/signtool) для подписания пакета приложения. Дополнительные сведения см. [в разделе как подписать пакет приложения с помощью средства SignTool](how-to-sign-a-package-using-signtool.md). Но сертификат по-прежнему не является доверенным для локального компьютера для развертывания пакетов приложений, пока он не будет установлен в хранилище доверенных сертификатов на локальном компьютере. Вы можете использовать [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), входящий в состав Windows.

**Установка сертификатов с помощью WindowsCertutil.exe**

1.  Запустите **Cmd.exe** от имени администратора.
2.  Выполните следующую команду:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Рекомендуется удалить сертификаты, если они больше не используются. В той же командной строке администратора выполните следующую команду:

``` syntax
Certutil -delStore TrustedPeople certID
```

**CertID** — серийный номер сертификата. Выполните следующую команду, чтобы определить серийный номер сертификата:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Соображения безопасности

Добавив сертификат в [хранилища сертификатов локальной машины](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), вы меняете доверие сертификатов всех пользователей на компьютере. Рекомендуется установить все сертификаты подписи кода, необходимые для тестирования пакетов приложений в хранилище сертификатов "Доверенные лица". Немедленно удалите эти сертификаты, когда они больше не нужны, чтобы предотвратить их использование для компрометации доверия системы.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Примеры**
</dt> <dt>

[Пример создания пакета приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Основные понятия**
</dt> <dt>

[Рекомендации по подписывания кода](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Подписывание пакета приложения с помощью SignTool)
</dt> <dt>

[Подписание пакета приложения](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 