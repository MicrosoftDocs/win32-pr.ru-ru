---
description: Включает создание и изменение индекса для указанной базы данных.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: Функция Сдбстартиндексинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141246"
---
# <a name="sdbstartindexing-function"></a>Функция Сдбстартиндексинг

Включает создание и изменение индекса для указанной базы данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*иивхич* \[ окне\]
</dt> <dd>

Идентификатор индекса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбкоммитиндексес**](sdbcommitindexes.md)
</dt> <dt>

[**сдбдеклареиндекс**](sdbdeclareindex.md)
</dt> <dt>

[**сдбстопиндексинг**](sdbstopindexing.md)
</dt> </dl>

 

 




