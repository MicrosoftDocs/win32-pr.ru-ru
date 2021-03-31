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
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784128"
---
# <a name="wmcontainerformat"></a>WM/Контаинерформат

Атрибут **WM/контаинерформат** указывает тип файла, который загружается в вызывающий объект.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмконтаинерформат

## <a name="data-type"></a>Тип данных

[**ВМТ \_ \_Формат хранения**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ \_ двоичный тип ВМТ**)

## <a name="remarks"></a>Комментарии

Этот атрибут используется вместо **IWMProfile3:: жетсторажеформат** и **IWMProfile3:: сетсторажеформат**, которые больше не поддерживаются.

Это закодированный атрибут.

Этот атрибут не может дублироваться на уровне файла. Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




