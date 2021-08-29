---
description: Завершает операции записи для указанного списка.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Функция Сдбендврителисттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9367b3c807cf152ab0c7aeb35a0b6d0e93ea03bbd10ea0dacb327030e21553c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076028"
---
# <a name="sdbendwritelisttag-function"></a>Функция Сдбендврителисттаг

Завершает операции записи для указанного списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл в, out\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*тилист* \[ окне\]
</dt> <dd>

[**TAGID**](tagid.md) списка

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Remarks

Вызовите эту функцию после записи всех записей списка. Он помечает конец списка.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдббегинврителисттаг**](sdbbeginwritelisttag.md)
</dt> <dt>

[**сдбклоседатабасе**](sdbclosedatabase.md)
</dt> <dt>

[**сдбклоседатабасеврите**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




