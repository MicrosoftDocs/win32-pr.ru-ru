---
description: Объявляет новый индекс в указанной базе данных.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Функция Сдбдеклареиндекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: b428699641d5a18bad8a1869f59ab1bb5402e7b667526070c3dc0575e435fc38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666593"
---
# <a name="sdbdeclareindex-function"></a>Функция Сдбдеклареиндекс

Объявляет новый индекс в указанной базе данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*твхич* \[ окне\]
</dt> <dd>

Этот параметр должен быть **\_ \_ списком типов тегов**.

</dd> <dt>

*tKey* \[ окне\]
</dt> <dd>

ТЕГ, указывающий тип, который будет использоваться в качестве ключа. Этот параметр не может **быть \_ \_ списком типов тегов**.

</dd> <dt>

*двентриес* \[ окне\]
</dt> <dd>

Число записей для выделения в индексе.

</dd> <dt>

*буникуекэй* \[ окне\]
</dt> <dd>

Если этот параметр имеет **значение true**, то индекс является индексом уникального ключа.

</dd> <dt>

*пиииндекс* \[ заполняет\]
</dt> <dd>

Результирующий **индексид** только что объявленного индекса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Remarks

Вызовите эту функцию перед записью тегов в новый индекс.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**индексид**](indexid.md)
</dt> <dt>

[**сдбкоммитиндексес**](sdbcommitindexes.md)
</dt> <dt>

[**сдбстартиндексинг**](sdbstartindexing.md)
</dt> <dt>

[**сдбстопиндексинг**](sdbstopindexing.md)
</dt> </dl>

 

 




