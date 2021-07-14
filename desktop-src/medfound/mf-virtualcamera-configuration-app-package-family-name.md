---
description: Указывает имя семейства пакетов приложений для приложения конфигурации виртуальной камеры.
title: Атрибут MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME (Мфапи. h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691869"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>\_ \_ \_ \_ Атрибут имени семейства пакетов приложений MF виртуалкамера \_

Указывает имя семейства пакетов приложений для приложения конфигурации виртуальной камеры. если этот параметр указан, конвейер свяжет приложение конфигурации с виртуальной камерой и предоставит точку запуска на странице Параметры камеры.

## <a name="data-type"></a>Тип данных

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>Комментарии

Этот атрибут может быть предоставлен с помощью настраиваемого источника мультимедиа виртуальной камеры из источника данных в хранилище атрибутов [имфмедиасаурцеекс:: жетсаурцеаттрибутес](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).  

Если приложение конфигурации еще не установлено на компьютере, приложение магазина будет запущено и откроется страница приложения, указанная с помощью имени семейства пакетов. В противном случае установленное приложение будет запущено для пользователя.


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Сборка 22000<br/>                          |
| Минимальная версия сервера<br/> | Windows Сборка 22000<br/>                      |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Имфаттрибутес:: SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




