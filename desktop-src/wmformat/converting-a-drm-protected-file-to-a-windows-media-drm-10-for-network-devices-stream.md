---
title: Преобразование файла DRM-Protected в поток Windows Media DRM 10 для сетевых устройств
description: Преобразование файла DRM-Protected в поток Windows Media DRM 10 для сетевых устройств
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK, преобразование файлов, защищенных с использованием DRM
- Windows Media Format SDK, файлы, защищенные с использованием DRM
- Расширенный формат систем (ASF), преобразование файлов, защищенных с использованием DRM
- ASF (Расширенный системный формат), преобразование файлов, защищенных с использованием DRM
- Расширенный формат систем (ASF), файлы, защищенные с использованием DRM
- ASF (Расширенный системный формат), файлы, защищенные с использованием DRM
- Управление цифровыми правами (DRM), преобразование файлов, защищенных с использованием DRM
- DRM (Управление цифровыми правами), преобразование файлов, защищенных с использованием DRM
- Управление цифровыми правами (DRM), файлы, защищенные с использованием DRM
- DRM (Управление цифровыми правами), файлы, защищенные с использованием DRM
- Windows Media Format SDK, Windows Media DRM 10 для сетевых устройств
- Windows Media Format SDK, DRM 10 для сетевых устройств
- Расширенный формат систем (ASF), Windows Media DRM 10 для сетевых устройств
- ASF (Расширенный системный формат), Windows Media DRM 10 для сетевых устройств
- Расширенный формат систем (ASF), DRM 10 для сетевых устройств
- ASF (Расширенный системный формат), DRM 10 для сетевых устройств
- Управление цифровыми правами (DRM), Windows Media DRM 10 для сетевых устройств
- DRM (Управление цифровыми правами), Windows Media DRM 10 для сетевых устройств
- Управление цифровыми правами (DRM), DRM 10 для сетевых устройств
- DRM (Управление цифровыми правами), DRM 10 для сетевых устройств
- Windows Media DRM 10 для сетевых устройств, преобразование файлов, защищенных с использованием DRM
- DRM 10 для сетевых устройств, преобразование файлов, защищенных с использованием DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788839"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>Преобразование файла DRM-Protected в поток Windows Media DRM 10 для сетевых устройств

После регистрации и проверки устройства можно начать обработку сообщений с запросами лицензий. Сообщения о запросах лицензий отправляются устройствами, когда требуется действие из приложения. В настоящее время поддерживается только действие "Воспроизвести", которое представляет собой запрос на защиту данных для воспроизведения.

При получении сообщения с запросом лицензии необходимо выполнить следующие действия.

1.  Проанализируйте сообщение с запросом лицензии, вызвав метод [**ивмдрммессажепарсер::P арселиценсерекуестмсг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) .
2.  Получите интерфейс [**ивмрегистереддевице**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) для устройства, вызвав метод [**Ивмдевицерегистратион:: жетрегистереддевицебид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , передав сертификат и серийный номер, полученные на шаге 1.
3.  Убедитесь, что устройство готово к получению защищенных данных:
    -   Вызовите [**ивмрегистереддевице:: утвердил**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) , чтобы убедиться, что устройство утверждено. Утверждение всегда должно основываться на предпочтениях пользователя.
    -   Вызовите [**ивмрегистереддевице:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) , чтобы убедиться, что устройство проверено в течение последних 48 часов. Если устройство является недопустимым, необходимо выполнить обнаружение близлежащих устройств. Дополнительные сведения см. в разделе [выполнение обнаружения близлежащих](performing-proximity-detection.md)устройств.
    -   Вызовите метод [**ивмрегистереддевице:: OnOpen**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) , чтобы убедиться, что устройство открыто. Если устройство не открыто, его можно открыть, вызвав [**ивмрегистереддевице:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). На компьютере может быть открыто только 10 устройств. Возможно, потребуется закрыть другое устройство, прежде чем можно будет открыть тот, для которого обрабатывается запрос. Чтобы закрыть устройство, вызовите метод [**ивмрегистереддевице:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) .
4.  Создайте экземпляр объекта перешифрования DRM, вызвав функцию [**вмкреатедрмтранскриптор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) .
5.  Вызовите метод [**ивмдрмтранскриптор:: Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) для инициализации перешифрования. Этот метод принимает указатель на реализацию интерфейса [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) , который используется для доставки сообщений о состоянии. Этот метод также возвращает сообщение о запросе лицензии, которое необходимо отправить на устройство, прежде чем продолжить.
6.  Когда метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) приложения получает \_ \_ сообщение о состоянии инициализации ВМТ, вызовите метод [**ивмдрмтранскриптор:: Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) , чтобы найти соответствующую начальную точку в файле. Чтобы начать с начала файла, необходимо вызвать **Seek** с Time 0.
7.  \_ \_ При готовности к доставке данных из файла в новое время презентации оно отправляет сообщение с повмтм прешифровании. Выполните повторяющиеся вызовы метода [**ивмдрмтранскриптор:: Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) , чтобы получить преобразованные фрагменты данных мультимедиа. Каждый вызов является асинхронным и не завершается, пока не \_ \_ получено сообщение о считывании ВМТ. После получения сообщения данные можно отправить на принимающее устройство.
8.  При получении сообщения ВМТ- \_ шифрования \_ с сообщением о том, что для параметра *HR* установлено значение NS \_ S \_ \_ (EOF), весь файл считывается. На этом этапе вызовите метод [**ивмдрмтранскриптор:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) , чтобы закрыть файл и освободить ресурсы.
9.  Когда \_ \_ получено закрытое сообщение ВМТ-шифрования, можно освободить интерфейс [**ивмдрмтранскриптор**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .

> [!Note]  
> DRM не поддерживает версию этого пакета SDK на базе x64.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование протокола Windows Media DRM 10 для сетевых устройств**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




