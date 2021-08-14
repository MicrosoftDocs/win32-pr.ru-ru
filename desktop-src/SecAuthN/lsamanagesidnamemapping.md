---
UID: ''
title: Функция Лсаманажесиднамемаппинг
description: Добавляет или удаляет сопоставления SID и имен из набора сопоставлений, зарегистрированного в службе LSA Lookup.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 6c2a66a318076588b725f74e9f03a23b8a134595b196dbf140850e72a7d78d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921863"
---
# <a name="lsamanagesidnamemapping-function"></a>Функция Лсаманажесиднамемаппинг

## <a name="description"></a>Описание

Функция **лсаманажесиднамемаппинг** добавляет или УДАЛЯЕТ сопоставления SID/имени из набора сопоставлений, зарегистрированного в службе LSA Lookup.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Параметры

### <a name="optype-in"></a>OpType [in]

Указывает, вызывается ли эта функция для добавления или удаления сопоставления SID и имени.

### <a name="opinput-in"></a>Опинпут [in]

Указывает значения домена, учетной записи и идентификатора безопасности, используемые во время этой операции. В этой структуре также можно задать дополнительные флаги.

### <a name="opoutput-out"></a>Опаутпут [out]

Содержит значение [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) , показывающее успешность операции или сбой.

| Значение | Значение |
|-------|---------|
| **Успешно** | Операция завершена без ошибок. |
| **нонмаппинжеррор** | Произошла ошибка, не связанная с сопоставлением имени SID. |
| **намеколлисион** | Сбой операции из-за конфликта имен. |
| **сидколлисион** | Сбой операции из-за конфликта SID. |
| **DomainNotFound** | Соответствующий домен не найден. |
| **домаинсидпрефиксмисматч** | Указанный идентификатор безопасности не имеет правильного префикса домена. |
| **маппингнотфаунд** | Сопоставление не найдено в кэше. |

## <a name="returns"></a>Возвращаемое значение

Если сопоставление успешно вставлено, возвращаемое значение будет STATUS_SUCCESS.
В противном случае, если функция завершилась ошибкой из-за конфликта SID или имени, будет возвращена STATUS_INVALID_PARAMETER ошибка.

## <a name="remarks"></a>Remarks

## <a name="see-also"></a>См. также раздел
