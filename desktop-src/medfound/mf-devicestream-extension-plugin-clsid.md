---
description: Указывает идентификатор CLSID подключаемого модуля последующей обработки для устройства видеозаписи.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Атрибут MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692508"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>\_ \_ \_ Атрибут CLSID подключаемого модуля расширения девицестреам MF \_

Указывает идентификатор CLSID подключаемого модуля последующей обработки для устройства видеозаписи.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Подключаемый модуль последующей обработки — это файл MFT, который обрабатывает видеоизображение после его записи. Поставщик оборудования может включать подключаемый модуль последующей обработки в составе установочного пакета. Если это так, источник видеозаписи устанавливает \_ \_ \_ атрибут CLSID подключаемого модуля расширения MF девицестреам \_ в идентификатор CLSID подключаемого модуля.

Чтобы получить этот атрибут, выполните следующие действия.

1.  Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.
3.  Вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) InAttribute, чтобы получить атрибут.

Чтобы создать подключаемый модуль, вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
