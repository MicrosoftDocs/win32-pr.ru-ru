---
description: Объявляет объект как выбор любой константы, чтобы избежать избыточных перегрузок этого объекта, если он используется (и объявлен) в нескольких местах в библиотеке Директксмас.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Макрос КСМГЛОБАЛКОНСТ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be72254865aed46de86955c2a27a4d73351311c5aa63a44a6e218be7a3915d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118004"
---
# <a name="xmglobalconst-macro"></a>Макрос КСМГЛОБАЛКОНСТ

Объявляет объект как *Выбор любой* константы, чтобы избежать избыточных перегрузок этого объекта, если он используется (и объявлен) в нескольких местах в библиотеке директксмас.

## <a name="syntax"></a>Синтаксис

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Remarks

Использование КСМГЛОБАЛКОНСТ позволяет использовать спецификацию глобальных констант. Это позволяет уменьшить размер сегмента данных приложения, избежать создания избыточных объектов и уничтожения, а также сократить операции загрузки и сохранения.

## <a name="requirements"></a>Требования

**Заголовок:** Объявлено в Директксмас. h.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Макросы библиотеки Директксмас](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Глобальные константы в библиотеке Директксмас](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
