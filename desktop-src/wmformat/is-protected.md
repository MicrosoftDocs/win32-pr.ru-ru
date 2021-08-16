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
ms.openlocfilehash: c0759dfc781409a1331403c3b02c2645f6ad843925584eab2a55f31a0c8d31af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847421"
---
# <a name="is_protected"></a>\_Защищено

Атрибут **\_ protected** является атрибутом уровня файла, который указывает, защищено ли содержимое файла с помощью управления цифровыми правами (DRM).

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмпротектед

## <a name="data-type"></a>Тип данных

**\_bool типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Это закодированный атрибут. Получение этого свойства предоставляет те же сведения, что и вызов [**вмисконтентпротектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Этот атрибут не может дублироваться на уровне файла. если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать свое нормальное значение объектам из пакета SDK Windows Media Format.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




