---
title: /notlb, параметр
description: Параметр/notlb предотвращает создание файла библиотеки типов (TLB) компилятором MIDL.
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- MIDL/notlb Switch
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067524"
---
# <a name="notlb-switch"></a>/notlb, параметр

Параметр **/notlb** предотвращает создание файла библиотеки типов (TLB) компилятором MIDL.

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

По умолчанию компилятор MIDL создает TLB-файл при обнаружении оператора [**Library**](library.md) . Этот параметр переопределяет поведение по умолчанию.

Если указан параметр **/notlb** , все другие заглушки, заголовки и т. д. создаются обычным образом.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




