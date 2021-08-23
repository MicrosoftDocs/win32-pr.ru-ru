---
title: Защита файлов с помощью DRM версии 1
description: Защита файлов с помощью DRM версии 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Пакет SDK для формата мультимедиа, создание защищенных файлов
- Windows Пакет SDK для формата мультимедиа, защищенные файлы
- Расширенный формат систем (ASF), создание защищенных файлов
- ASF (Расширенный системный формат), создание защищенных файлов
- Расширенный формат систем (ASF), защищенные файлы
- ASF (Расширенный системный формат), защищенные файлы
- Расширенный системный формат (ASF), Вмстубдрм. lib
- ASF (Расширенный системный формат), Вмстубдрм. lib
- Вмстубдрм. lib, создание защищенных файлов
- Вмстубдрм. lib, защищенные файлы
- Управление цифровыми правами (DRM), Вмстубдрм. lib
- DRM (Управление цифровыми правами), Вмстубдрм. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b500f3711b8c92324cbd87d4dc199a8a0bb803cba69357a23f139fb96f8281f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084541"
---
# <a name="protecting-files-with-drm-version-1"></a>Защита файлов с помощью DRM версии 1

При применении этого типа защиты создается лицензия DRM версии 1, которая действительна только на компьютере, с которого был сделан запрос на лицензию. Поскольку начальное значение ключа или ключа не задано, невозможно создать переносимые лицензии для содержимого, защищенного с помощью этого метода. однако при использовании Windows Media Format SDK 7,1 или более поздней версии лицензии могут быть восстановлены в службе миграции лицензий майкрософт.

Чтобы защитить файлы ASF с помощью DRM версии 1, выполните следующие действия.

1.  Свяжите файл Вмстубдрм. lib с проектом и при необходимости отменяйте связь вмвкоре. lib.
2.  Чтобы создать модуль записи, вызовите функцию [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Первый аргумент зарезервирован и должен иметь значение **null**.
3.  Задайте профиль для модуля записи, который следует использовать, вызвав [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) или [**Ивмвритер:: сетпрофилебид**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Перед установкой атрибутов DRM необходимо задать профиль в модуле записи. DRM поддерживается только для профилей, использующих видеокодеки Windows media Audio или Windows media Video.
4.  С помощью метода [**ивмхеадеринфо:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) задайте следующие свойства DRM. Свойство **USE \_ DRM** указывает компоненту DRM защищать содержимое с помощью DRM версии 1. Свойство **\_ flags DRM** указывает права, которые должны быть добавлены в локальную лицензию, которая будет создана для содержимого. Значение **\_ уровня DRM** также хранится в лицензии; оно указывает минимальный уровень, необходимый для доступа к содержимому. 150 — рекомендуемый уровень содержимого для DRM версии 1.

    | attribute      | Значение                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Использование \_ DRM**   | **TRUE**                                                                                    |
    | **\_Флаги DRM** | ВМТ \_ right \_ Воспроизведение \| ВМТ \_ права \_ копирования \_ на \_ \_ устройство без \_ SDMI \| ВМТ \_ право \_ Копировать \_ на \_ компакт-диск |
    | **\_уровень DRM** | 150                                                                                         |

    

     

В следующем примере кода показано, как создать модуль записи с поддержкой DRM для DRM версии 1 и задать свойства DRM. В целях уточнения пропущена проверка ошибок.


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




