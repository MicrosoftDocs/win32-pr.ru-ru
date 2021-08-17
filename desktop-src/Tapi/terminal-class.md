---
description: Идентификаторы GUID класса терминала определяют конкретный терминал по возможностям.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Класс Terminal (Tapi3if. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd20d3e540529b343d1fb848b9e8cb2579a621b40146e0d170fdb175c4c9a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975454"
---
# <a name="terminal-class"></a>Класс терминала

Идентификаторы GUID класса терминала определяют конкретный терминал по возможностям.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**\_ФИЛЕПЛАЙБАККТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Терминал воспроизведения файлов.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**\_ФИЛЕРЕКОРДИНГТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Терминал записи файлов.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**\_ФИЛЕРЕКОРДИНГТРАКК CLSID**
</dt> <dd> <dl> <dt>



Запись файла.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**\_ХАНДСЕТТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Телефонная трубка.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**\_ХЕАДСЕТТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Головной набор.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**\_МЕДИАСТРЕАМТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Терминал потока мультимедиа, динамически создаваемый.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**\_МИКРОФОНЕТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Звук.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**\_СПЕАКЕРФОНЕТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Телефон динамика.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**\_СПЕАКЕРСТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Используют.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**\_ВИДЕОИНПУТТЕРМИНАЛ CLSID**
</dt> <dd> <dl> <dt>



Терминал входного видео.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**\_ВИДЕОВИНДОВТЕРМ CLSID**
</dt> <dd> <dl> <dt>



Окно просмотра видео, созданное динамически.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

версия **BSTR** классов терминалов в основном предназначена для использования Visual Basic приложений. (Например, они возвращаются в виде элементов коллекции, полученной с помощью [**Get \_ динамиктерминалклассес**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses).)

-   Хандсеттерминал строка CLSID для BSTR \_ \_
-   Хеадсеттерминал строка CLSID для BSTR \_ \_
-   Медиастреамтерминал строка CLSID для BSTR \_ \_
-   Микрофонетерминал строка CLSID для BSTR \_ \_
-   Спеакерфонетерминал строка CLSID для BSTR \_ \_
-   Спеакерстерминал строка CLSID для BSTR \_ \_
-   Видеоинпуттерминал строка CLSID для BSTR \_ \_
-   Видеовиндовтерм строка CLSID для BSTR \_ \_

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|--------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                |
| Заголовок<br/>       | <dl> <dt>Tapi3if. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иттерминалсуппорт:: Креатетерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**Иттерминал:: Get \_ терминалкласс**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**Иттерминалманажер:: Креатединамиктерминал**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**Иттерминалманажер:: Жетдинамиктерминалклассес**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**Иттерминалсуппорт:: Енумератединамиктерминалклассес**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

