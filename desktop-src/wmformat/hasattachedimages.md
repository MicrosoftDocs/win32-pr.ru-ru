---
title: хасаттачедимажес
description: Атрибут Хасаттачедимажес представляет собой атрибут уровня файла, указывающий, является ли файл MP3-файлом с подключенными кадрами APIC ID3.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Формат Windows Media Хасаттачедимажес
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ec38d0961ffc6ffc50434cdecf69e6dde663dfeaff5e331455a9575b3426e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930864"
---
# <a name="hasattachedimages"></a>хасаттачедимажес

Атрибут **хасаттачедимажес** представляет собой атрибут уровня файла, указывающий, является ли файл MP3-файлом с подключенными КАДРАМИ APIC ID3.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмхасаттачедимажес

## <a name="data-type"></a>Тип данных

**\_bool типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Это закодированный атрибут.

Этот атрибут не может дублироваться на уровне файла. если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать свое нормальное значение объектам из пакета SDK Windows Media Format.

**Хасаттачедимажес** был разработан для информирования приложения о наличии изображений, чтобы их можно было получить с помощью интерфейса [**ивмимажеинфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Теперь, когда образы поддерживаются с помощью атрибута [**WM/Picture**](wmpicture.md) , **хасаттачедимажес** больше не требуется.

Чтобы определить, содержит ли файл изображения, вызовите [**IWMHeaderInfo3:: жетаттрибутеиндицес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) , указав атрибут **WM/Picture** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




