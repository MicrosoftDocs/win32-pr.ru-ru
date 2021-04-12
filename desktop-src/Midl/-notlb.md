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
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487145"
---
# <a name="notlb-switch"></a>/notlb, параметр

Параметр **/notlb** предотвращает создание файла библиотеки типов (TLB) компилятором MIDL.

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

По умолчанию компилятор MIDL создает TLB-файл при обнаружении оператора [**Library**](library.md) . Этот параметр переопределяет поведение по умолчанию.

Если указан параметр **/notlb** , все другие заглушки, заголовки и т. д. создаются обычным образом.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




