---
title: WM/Контаинерформат
description: Атрибут WM/Контаинерформат указывает тип файла, который загружается в вызывающий объект.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Формат Windows Media WM/Контаинерформат
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839444"
---
# <a name="wmcontainerformat"></a>WM/Контаинерформат

Атрибут **WM/контаинерформат** указывает тип файла, который загружается в вызывающий объект.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмконтаинерформат

## <a name="data-type"></a>Тип данных

[**ВМТ \_ \_Формат хранения**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ \_ двоичный тип ВМТ**)

## <a name="remarks"></a>Remarks

Этот атрибут используется вместо **IWMProfile3:: жетсторажеформат** и **IWMProfile3:: сетсторажеформат**, которые больше не поддерживаются.

Это закодированный атрибут.

Этот атрибут не может дублироваться на уровне файла. если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать свое нормальное значение объектам из пакета SDK Windows Media Format.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




