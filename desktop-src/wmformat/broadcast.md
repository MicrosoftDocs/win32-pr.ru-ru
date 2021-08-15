---
title: Широковещательное
description: Атрибут Broadcast является атрибутом уровня файла, указывающим, можно ли транслировать содержимое. Предполагается, что любое содержимое, для которого не назначен авторские права, может быть юридическим.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Формат вещания Windows Media
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b233a74deb71efe041ab5ad2f5e4ffa421d048a70c5b97e8f7ac38499bd18df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086172"
---
# <a name="broadcast"></a>Широковещательное

Атрибут **Broadcast** является атрибутом уровня файла, указывающим, можно ли транслировать содержимое. Предполагается, что любое содержимое, для которого не назначен авторские права, может быть юридическим.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмброадкаст

## <a name="data-type"></a>Тип данных

**\_bool типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Это закодированный атрибут.

Этот атрибут не может дублироваться на уровне файла. если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать свое нормальное значение объектам из пакета SDK Windows Media Format.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




