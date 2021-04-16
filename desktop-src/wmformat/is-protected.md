---
title: Is_Protected
description: '\_Атрибут protected является атрибутом уровня файла, который указывает, защищено ли содержимое файла с помощью управления цифровыми правами (DRM).'
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected формат Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710231"
---
# <a name="is_protected"></a>\_Защищено

Атрибут **\_ protected** является атрибутом уровня файла, который указывает, защищено ли содержимое файла с помощью управления цифровыми правами (DRM).

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмпротектед

## <a name="data-type"></a>Тип данных

**\_bool типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Это закодированный атрибут. Получение этого свойства предоставляет те же сведения, что и вызов [**вмисконтентпротектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Этот атрибут не может дублироваться на уровне файла. Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




