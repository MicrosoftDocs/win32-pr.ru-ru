---
description: Объявляет объект как выбор любой константы, чтобы избежать избыточных перегрузок этого объекта, если он используется (и объявлен) в нескольких местах в библиотеке Директксмас.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Макрос КСМГЛОБАЛКОНСТ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711475"
---
# <a name="xmglobalconst-macro"></a>Макрос КСМГЛОБАЛКОНСТ

Объявляет объект как *Выбор любой* константы, чтобы избежать избыточных перегрузок этого объекта, если он используется (и объявлен) в нескольких местах в библиотеке директксмас.

## <a name="syntax"></a>Синтаксис

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Примечания

Использование КСМГЛОБАЛКОНСТ позволяет использовать спецификацию глобальных констант. Это позволяет уменьшить размер сегмента данных приложения, избежать создания избыточных объектов и уничтожения, а также сократить операции загрузки и сохранения.

## <a name="requirements"></a>Требования

**Заголовок:** Объявлено в Директксмас. h.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Макросы библиотеки Директксмас](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Глобальные константы в библиотеке Директксмас](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
