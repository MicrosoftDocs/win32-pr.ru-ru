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
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691448"
---
# <a name="hasattachedimages"></a>хасаттачедимажес

Атрибут **хасаттачедимажес** представляет собой атрибут уровня файла, указывающий, является ли файл MP3-файлом с подключенными КАДРАМИ APIC ID3.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмхасаттачедимажес

## <a name="data-type"></a>Тип данных

**\_bool типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Это закодированный атрибут.

Этот атрибут не может дублироваться на уровне файла. Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.

**Хасаттачедимажес** был разработан для информирования приложения о наличии изображений, чтобы их можно было получить с помощью интерфейса [**ивмимажеинфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Теперь, когда образы поддерживаются с помощью атрибута [**WM/Picture**](wmpicture.md) , **хасаттачедимажес** больше не требуется.

Чтобы определить, содержит ли файл изображения, вызовите [**IWMHeaderInfo3:: жетаттрибутеиндицес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) , указав атрибут **WM/Picture** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




