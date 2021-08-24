---
UID: ''
title: Функция Шисчилдорселф
description: Сравнивает, является ли окно равным, дочерним элементом или потомком второго окна.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2d8eaab0f17647a6f548a0243199073baef074c88dad6a3f7100cfbca1a02be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941334"
---
# <a name="shischildorself-function"></a>Функция Шисчилдорселф

## <a name="description"></a>Описание

\[эта функция доступна в Windows XP и Windows Server 2003.
Он может быть изменен или недоступен в последующих версиях Windows.\]

Сравнивает, является ли окно равным, дочерним элементом или потомком второго окна.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Параметры

### <a name="hwndparent-in"></a>Хвндпарент [in]

Тип: **HWND**

Маркер первого окна.

### <a name="hwnd-in"></a>HWND [в]

Тип: **HWND**

Описатель для окна, проверяемого на соответствие *хвндпарент*.

## <a name="returns"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает **S_OK** , если окно, заданное параметром *HWND* , равно, дочерний элемент или потомок окна, заданного параметром *хвндпарент*.
Возвращает **S_FALSE** , если окно, заданное HWND, не равно, а не является дочерним элементом, а не является потомком окна, заданного параметром *хвндпарент*.
Возвращаемое значение не определено, если один из окон является недопустимым.

## <a name="remarks"></a>Remarks

## <a name="see-also"></a>См. также

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
