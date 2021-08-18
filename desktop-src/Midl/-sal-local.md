---
title: sal_local Switch
description: '\_Локальный коммутатор/Сал направляет MIDL для создания аннотаций SAL для параметров методов интерфейса, помеченных \ Local \. Также должен присутствовать параметр/Сал.'
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local параметр MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666401cca482846fc2e6a9d5851a4da9d2d362279c9bc1496ab672a94ac9b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014092"
---
# <a name="sal_local-switch"></a>\_локальный коммутатор/Сал

**\_ Локальный коммутатор/Сал** направляет MIDL для создания аннотаций SAL для параметров методов интерфейса, помеченных как [**\[ локальные \]**](local.md). Также должен присутствовать параметр [**/Сал**](-sal.md) .

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

Изменяет поведение параметра [**/Сал**](-sal.md) , чтобы также предоставить заметки для параметров методов интерфейса, помеченных [**\[ локальным \]**](local.md) атрибутом. Используйте атрибут [**\[ аннотации \]**](annotate.md), чтобы переопределить созданную с помощью MIDL аннотацию другой строкой заметки.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/сал**](-sal.md)
</dt> <dt>

[**\[комментировани\]**](annotate.md)
</dt> </dl>

 

 




