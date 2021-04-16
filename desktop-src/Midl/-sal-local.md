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
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672197"
---
# <a name="sal_local-switch"></a>\_локальный коммутатор/Сал

**\_ Локальный коммутатор/Сал** направляет MIDL для создания аннотаций SAL для параметров методов интерфейса, помеченных как [**\[ локальные \]**](local.md). Также должен присутствовать параметр [**/Сал**](-sal.md) .

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

Изменяет поведение параметра [**/Сал**](-sal.md) , чтобы также предоставить заметки для параметров методов интерфейса, помеченных [**\[ локальным \]**](local.md) атрибутом. Используйте атрибут [**\[ аннотации \]**](annotate.md), чтобы переопределить созданную с помощью MIDL аннотацию другой строкой заметки.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/сал**](-sal.md)
</dt> <dt>

[**\[комментировани\]**](annotate.md)
</dt> </dl>

 

 




