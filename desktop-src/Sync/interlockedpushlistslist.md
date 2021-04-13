---
UID: ''
title: Функция InterlockedPushListSList
description: Вставляет однонаправленный список в начале другого однонаправленного списка.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "104412716"
---
# <a name="interlockedpushlistslist-function"></a>Функция InterlockedPushListSList

## <a name="description"></a>Описание

Вставляет однонаправленный список в начале другого однонаправленного списка.
Доступ к спискам синхронизируется в многопроцессорной системе.

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>Параметры

### <a name="listhead-in-out"></a>Лиссеад [вход, выход]

Указатель на структуру **SLIST_HEADER** , представляющую собой заголовок однонаправленного списка.
Список, указанный в *списке* и *прослушиваемых* параметрах, вставляется в начало этого списка.

### <a name="list-in-out"></a>List [входные и выходные]

Указатель на структуру [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) , представляющую первый элемент в списке для вставки.

### <a name="listend-in-out"></a>ListEned [вход, выход]

Указатель на структуру [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) , представляющую последний элемент в вставляемом списке.

### <a name="count-in"></a>Число [в]

Число вставляемых элементов в списке.

## <a name="returns"></a>Возвращаемое значение

Возвращаемое значение — это предыдущий первый элемент в списке, заданном параметром *лиссеад* .
Если список был ранее пустым, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

Все элементы списка должны быть согласованы по границе **MEMORY_ALLOCATION_ALIGNMENT** ; в противном случае эта функция будет вести себя непредсказуемым образом.
См. **_aligned_malloc**.

**Windows 8 и Windows Server 2012:**  Эта функция была заменена [интерлоккедпушлистслистекс](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).
При компиляции с **NTDDI_VERSION** , для которого задано значение **NTDDI_WIN8** или больше, вызовы **Интерлоккедпушлистслист** будут переходят в **интерлоккедпушлистслистекс** .

## <a name="see-also"></a>См. также раздел

[Взаимозаблокированные однонаправленные списки](/windows/desktop/Sync/interlocked-singly-linked-lists)

[интерлоккедпопентрислист](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[интерлоккедпушентрислист](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[интерлоккедпушлистслистекс](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[интерлоккедфлушслист](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Использование однонаправленных списков](/windows/desktop/Sync/using-singly-linked-lists)
