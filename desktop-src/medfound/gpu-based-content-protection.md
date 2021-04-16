---
description: Описание содержимого видео&\# 8211, возможностей защиты, которые может предоставить графический драйвер.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based Защита содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc1a0f88cae199b9aab38e5ec429ea5427f44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550431"
---
# <a name="gpu-based-content-protection"></a>GPU-Based Защита содержимого

В этом разделе описывается содержимое видео — возможности защиты, которые может предоставить графический драйвер.

-   [Введение](#introduction)
-   [Общие сведения о процессе декодирования](#overview-of-the-decoding-process)
-   [Шифрование сжатых буферов видео для декодера](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. запросите Защита содержимого возможности драйвера.](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Настройка канала, прошедшего проверку подлинности](#2-configure-the-authenticated-channel)
    -   [3. Настройка сеанса шифрования](#3-configure-the-cryptographic-session)
    -   [4. получение маркера для устройства декодера ДКСВА](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. Связывание декодера ДКСВА с криптографическим сеансом](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Отправка команд аутентифицированного канала](#sending-authenticated-channel-commands)
-   [Отправка запросов к каналам с проверкой подлинности](#sending-authenticated-channel-queries)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

На следующей диаграмме показано упрощенное представление того, как защищенное видео проходит через конвейер для подготовки к просмотру.

![Схема, на которой показано защищенное видео-содержимое.](images/d3d9video01.png)

> [!Note]  
> [Путь к защищенному носителю](protected-media-path.md) (PMP) не показан на этой схеме. Показанный здесь поток данных может находиться в процессе PMP или в процессе приложения.

 

Декодер получает зашифрованные сжатые данные видео из внешнего источника. Предполагается, что декодер также получает криптографический ключ для расшифровки этих данных. В этом разделе не описывается обмен ключами между источником видео и декодером, но PMP определяет один из возможных механизмов. На этом этапе не участвует графический процессор.

При декодировании с аппаратным ускорением программный декодер передает сжатое видео-изображение в графический процессор. Чтобы защитить это содержимое, декодер повторно шифрует данные, как правило, с помощью AES-Protector, перед передачей их в аппаратный ускоритель. Механизм обмена ключами определяется между декодером и драйвером графики.

Декодированные видеоматериалы хранятся в видеопамяти, как правило, в четком виде. На этом этапе кадры обрабатываются, а затем представляются. Существует два основных варианта представления.

-   Фреймы можно представить с помощью наложения оборудования. Дополнительные сведения см. в разделе [поддержка наложения оборудования](hardware-overlay-support.md).
-   Фреймы могут быть представлены оконным окном Управление (DWM) с помощью общей поверхности.

Последним шагом является отображение кадра на мониторе, для которого может потребоваться защита канала между графической картой и устройством отображения. Примером защиты канала является High-Bandwidth цифровой Защита содержимого (HDCP). Защита канала настраивается с помощью [диспетчера выходной защиты](output-protection-manager.md) (ОПМ). В этом разделе не описывается ОПМ; Дополнительные сведения см. [в разделе Использование диспетчера выходной защиты](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Общие сведения о процессе декодирования

При декодировании с аппаратным ускорением программный декодер должен передавать на графическую карту сжатые данные видео. Для содержимого уровня "Премиум" эти данные обычно должны быть зашифрованы с помощью шифрования с симметричным ключом перед отправкой на GPU.

Чтобы зашифровать видео для декодирования, программный декодер использует следующие интерфейсы:

-   [**Идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Представляет устройство декодера ДКСВА, также называемое ускорителем.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Представляет сеанс шифрования, который предоставляет ключ шифрования.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Представляет канал, прошедший проверку подлинности, который позволяет декодеру программного обеспечения связывать сеанс шифрования с декодером ДКСВА.

![Схема, на которой показаны интерфейсы декодирования Direct3D9.](images/d3d9video02.png)

Все эти интерфейсы получаются с устройства Direct3D следующим образом:



| Интерфейс                                                                | Создание                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Вызовите [**идиректксвидеодекодерсервице:: креатевидеодекодер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Устройство декодера ДКСВА определяется идентификатором GUID профиля ДКСВА. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Вызовите [**IDirect3DDevice9Video:: креатекриптосессион**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Вызовите [**IDirect3DDevice9Video:: креатеаусентикатедчаннел**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Чтобы получить указатель на интерфейс [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) , вызовите метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на устройстве D3D9Ex.

 

Прошедший проверку подлинности канал предоставляет доверенный канал связи между программным декодером и драйвером. Коммуникационный канал работает следующим образом:

-   Драйвер предоставляет цепочку сертификатов X. 509, корневой сертификат которой подписан корпорацией Майкрософт.
-   Сертификат содержит открытый ключ RSA для драйвера.
-   Программный декодер использует открытый ключ для отправки драйвера в 128-разрядный сеансовый ключ AES.
-   Программный декодер отправляет запросы и команды в канал, прошедший проверку подлинности.
-   Ключ сеанса используется для расчета кодов проверки подлинности сообщений (Mac) для запросов и команд. Драйвер использует макинтоши для проверки целостности данных запроса или команды, а программный декодер использует их для проверки целостности данных ответа из драйвера.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Шифрование сжатых буферов видео для декодера

Ниже приведен общий обзор процесса шифрования и декодирования.

1.  Программный декодер получает поток зашифрованных данных из источника видео. Декодер расшифровывает этот поток.
2.  Программный декодер согласовывает сеансовый ключ с сеансом шифрования.
3.  Программный декодер использует прошедший проверку подлинности канал для связи криптографического сеанса с устройством декодера ДКСВА.
4.  Программный декодер помещает сжатые данные в буферы ДКСВА, которые он получает с устройства декодера ДКСВА (Ускоритель). Для защищенного содержимого кодировщик шифрует данные, помещенные в буферы ДКСВА, используя ключ сеанса для шифрования.
    > [!Note]  
    > Некоторые драйверы используют ключ содержимого вместо ключа сеанса для шифрования. Ключ содержимого может меняться от одного кадра к другому.

     

5.  Декодер отправляет зашифрованные сжатые буферы в ускоритель. Для алгоритма AES-Ctrl декодер также передает вектор инициализации. Если используется ключ содержимого, декодер передает ключ содержимого, зашифрованный с помощью ключа сеанса.

В Direct3D предусмотрена стандартная поддержка 128-разрядного алгоритма AES-CTRL, но она предназначена для расширения дополнительных типов шифрования.

Следующие пять разделов содержат более подробные инструкции.

-   [1. запросите Защита содержимого возможности драйвера.](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Настройка канала, прошедшего проверку подлинности](#2-configure-the-authenticated-channel)
-   [3. Настройка сеанса шифрования](#3-configure-the-cryptographic-session)
-   [4. получение маркера для устройства декодера ДКСВА](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. Связывание декодера ДКСВА с криптографическим сеансом](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. запросите Защита содержимого возможности драйвера.

Прежде чем пытаться применить шифрование, получите возможности защиты содержимого драйвера.

1.  Получение указателя на устройство Direct3D 9.
2.  Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) .
3.  Вызовите [**IDirect3DDevice9Video:: жетконтентпротектионкапс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Этот метод заполняет структуру [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) с помощью возможностей защиты содержимого драйвера.

В частности, найдите следующие возможности:

-   Если элемент **Caps** содержит флаг **D3DCPCAPS_SOFTWARE** или **D3DCPCAPS_HARDWARE** , драйвер может выполнять шифрование.
-   Член **кэйексчанжетипе** задает способ выполнения обмена ключами для ключа сеанса.
-   Если элемент **Caps** содержит флаг **D3DCPCAPS_CONTENTKEY** , драйвер использует для шифрования отдельный ключ содержимого. Это важно при создании ключа сеанса.

Дополнительные возможности указываются в элементе « **Caps** ».

### <a name="2-configure-the-authenticated-channel"></a>2. Настройка канала, прошедшего проверку подлинности

Следующим шагом является настройка канала, прошедшего проверку подлинности.

1.  Вызовите [**IDirect3DDevice9Video:: креатеаусентикатедчаннел**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) , чтобы создать канал с проверкой подлинности. Для параметра *чаннелтипе* укажите тип канала, соответствующий возможностям драйвера.
    -   Тип канала **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** соответствует **D3DCPCAPS_SOFTWARE**.
    -   Тип канала **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** соответствует **D3DCPCAPS_HARDWARE**.

    Метод **креатеаусентикатедчаннел** возвращает указатель на интерфейс [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) вместе с маркером для канала. Этот маркер используется позже для связывания сеанса шифрования с аутентифицированным каналом.
2.  Вызовите [**IDirect3DAuthenticatedChannel9:: жетцертификатесизе**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) , чтобы получить размер сертификата X. 509 драйвера. Выделение буфера требуемого размера.
3.  Вызовите [**IDirect3DAuthenticatedChannel9:: Certificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) , чтобы получить сертификат. Метод копирует сертификат в буфер, который был выделен на предыдущем шаге.
4.  Убедитесь, что сертификат драйвера был подписан корпорацией Майкрософт и не был отозван.
5.  Получите открытый ключ из сертификата.
6.  Создание случайного ключа сеанса RSA. Этот ключ сеанса используется для подписывания данных, отправляемых в канал, прошедший проверку подлинности. Зашифруйте сеансовый ключ с помощью открытого ключа драйвера.
7.  Вызовите метод [**IDirect3DAuthenticatedChannel9:: неготиатекэйексчанже**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) , чтобы отправить зашифрованный ключ сеанса драйверу.
8.  Инициализируйте безопасный канал следующим образом:
    1.  Заполните структуру [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) , как описано в документации.
    2.  Отправьте команду [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) , вызвав [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) , как описано в разделе [Отправка команд, прошедших проверку подлинности канала](#sending-authenticated-channel-commands). Эта команда содержит начальные порядковые номера для команд и запросов, отправляемых в канал, прошедший проверку подлинности.
9.  Проверьте тип канала, отправив запрос [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) в канал, прошедший проверку подлинности, как описано в разделе [Отправка запросов с проверкой подлинности](#sending-authenticated-channel-queries). Убедитесь, что тип канала соответствует тому, что вы указали в методе [**креатеаусентикатедчаннел**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. Настройка сеанса шифрования

Затем настройте сеанс шифрования и установите ключ сеанса.

1.  Вызовите [**IDirect3DDevice9Video:: креатекриптосессион**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) , чтобы создать сеанс шифрования. Этот метод возвращает указатель на интерфейс [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) , а также на обработку сеанса шифрования.
2.  Вызовите [**IDirect3DCryptoSession9:: жетцертификатесизе**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) , чтобы получить размер сертификата X. 509 драйвера. Выделение буфера требуемого размера.
3.  Вызовите [**IDirect3DCryptoSession9:: Certificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) , чтобы получить сертификат. Метод копирует сертификат в буфер, который был выделен на предыдущем шаге.
4.  Убедитесь, что сертификат драйвера был подписан корпорацией Майкрософт и не был отозван.
5.  Получите открытый ключ из сертификата.
6.  Создание случайного ключа сеанса RSA. Это отдельный сеансовый ключ из ключа сеанса прошедшего проверку подлинности канала. Зашифруйте сеансовый ключ с помощью открытого ключа драйвера.
7.  Вызовите метод [**IDirect3DCryptoSession9:: неготиатекэйексчанже**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) , чтобы отправить зашифрованный ключ сеанса драйверу.
8.  Если возможности защиты содержимого включают **D3DCPCAPS_CONTENTKEY**, создайте случайный ключ содержимого RSA. Он будет использоваться позже в процессе декодирования.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. получение маркера для устройства декодера ДКСВА

Для следующего шага потребуется обработчик для устройства декодера ДКСВА. Чтобы получить этот маркер, заполните структуру DXVA2_DecodeExecuteParams следующим образом:


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



Задайте для элемента **пекстенсиондата** структуры [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) адрес структуры [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) .

В структуре [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) задайте для члена **функции** значение **DXVA2_DECODE_GET_DRIVER_HANDLE**. Задайте **пприватеаутпутдата** в качестве адреса буфера, достаточного размера для хранения значения **Handle** . (В предыдущем примере этот буфер является переменной *хдекодедевицехандле* .)

Затем вызовите [**идиректксвидеодекодер:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) и передайте адрес структуры [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) . Обработчик для декодера ДКСВА возвращается в **пприватеаутпутдата**.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. Связывание декодера ДКСВА с криптографическим сеансом

Затем свяжите устройство декодера ДКСВА с устройством Direct3D и сеансом шифрования следующим образом:

1.  Получите маркер устройства декодера ДКСВА, как описано в предыдущем разделе.
2.  Получите маркер устройства Direct3D, отправив запрос [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) в канал, прошедший проверку подлинности.
3.  Заполните структуру [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) следующими сведениями:
    -   Задайте для элемента **DXVA2DecodeHandle** маркер устройства декодера дксва.
    -   Задайте для элемента **криптосессионхандле** маркер сеанса шифрования. Этот маркер возвращается методом [**IDirect3DDevice9Video:: креатекриптосессион**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) .
    -   Задайте для элемента **девицехандле** маркер устройства Direct3D.
4.  Вызовите [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) , чтобы отправить в канал, прошедший проверку подлинности, [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) команду.

На следующей схеме показан обмен дескрипторами:

![Схема, показывающая, как декодер дксва связан с сеансом шифрования.](images/d3d9video03.png)

Теперь программный декодер может использовать криптографический ключ сеанса для шифрования сжатых буферов видео. Каждый сжатый буфер будет иметь собственный вектор инициализации (IV), заданный в элементе **пвпвпстате** структуры [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) .

## <a name="sending-authenticated-channel-commands"></a>Отправка команд аутентифицированного канала

Набор команд определяется для настройки аутентифицированного канала и настройки различных параметров защиты содержимого. Список команд см. в разделе [Защита содержимого Commands](content-protection-commands.md).

Чтобы отправить команду в канал, прошедший проверку подлинности, выполните следующие действия.

1.  Заполните структуру входных данных. Эта структура данных всегда является структурой [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) , за которой следуют дополнительные поля. Заполните структуру **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** , как показано в следующей таблице.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Член</th>
    <th>Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>омак</strong></td>
    <td>Пока не пропустите это поле.</td>
    </tr>
    <tr class="even">
    <td><strong>конфигуретипе</strong></td>
    <td>Идентификатор GUID, идентифицирующий команду. Список команд см. в разделе <a href="content-protection-commands.md">Защита содержимого Commands</a>.</td>
    </tr>
    <tr class="odd">
    <td><strong>хчаннел</strong></td>
    <td>Маркер для аутентифицированного канала.</td>
    </tr>
    <tr class="even">
    <td><strong>SequenceNumber</strong></td>
    <td>Порядковый номер. Первый порядковый номер задается путем отправки команды <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Каждый раз, когда вы отправляете другую команду, увеличивайте это число на 1. Порядковый номер защищается от атак с использованием воспроизведения.
    <blockquote>
    [!Note]<br />
Используются два отдельных порядковых номера: один для команд и один для запросов.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Вычислите тег ОМАК для блока данных, который появляется после элемента **ОМАК** входной структуры. Затем скопируйте значение этого тега в элемент **ОМАК** .
3.  Вызовите [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  Драйвер помещает выходные данные команды в структуру [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) .
5.  Вычислите тег ОМАК для блока данных, который отображается после элемента **ОМАК** в выходной структуре. Сравните это со значением элемента **ОМАК** . Завершать с ошибкой, если они не совпадают.
6.  Сравните значения элементов **конфигуретипе**, **хчаннел** и **SequenceNumber** в выходной структуре со значениями для этих элементов. Завершать с ошибкой, если они не совпадают.
7.  Увеличение порядкового номера для следующей команды.

## <a name="sending-authenticated-channel-queries"></a>Отправка запросов к каналам с проверкой подлинности

Набор запросов определяется для получения сведений о канале, прошедшем проверку подлинности. Список запросов см. в разделе [запросы защита содержимого](content-protection-queries.md).

Чтобы отправить команду в канал, прошедший проверку подлинности, выполните следующие действия.

1.  Заполните структуру входных данных. Эта структура данных всегда является структурой [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) , возможно, за ней следуют дополнительные поля. Заполните структуру **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** , как показано в следующей таблице.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Член</th>
    <th>Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>QueryType</strong></td>
    <td>Идентификатор GUID, определяющий запрос. Список запросов см. в разделе <a href="content-protection-queries.md">запросы защита содержимого</a>.</td>
    </tr>
    <tr class="even">
    <td><strong>хчаннел</strong></td>
    <td>Маркер для аутентифицированного канала.</td>
    </tr>
    <tr class="odd">
    <td><strong>SequenceNumber</strong></td>
    <td>Порядковый номер. Первый порядковый номер задается путем отправки команды <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Каждый раз, когда вы отправляете другой запрос, увеличивайте это число на 1. Порядковый номер защищается от атак с использованием воспроизведения.
    <blockquote>
    [!Note]<br />
Используются два отдельных порядковых номера: один для команд и один для запросов.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Вызовите [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  Драйвер помещает выходные данные запроса в структуру [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) . За этой структурой следуют дополнительные поля в зависимости от типа запроса.
4.  Вычислите тег ОМАК для блока данных, который отображается после элемента **ОМАК** в выходной структуре. Сравните это со значением элемента **ОМАК** . Завершать с ошибкой, если они не совпадают.
5.  Сравните значения элементов **конфигуретипе**, **хчаннел** и **SequenceNumber** в выходной структуре со значениями для этих элементов. Завершать с ошибкой, если они не совпадают.
6.  Увеличение порядкового номера для следующего запроса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[API-интерфейсы видео Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
