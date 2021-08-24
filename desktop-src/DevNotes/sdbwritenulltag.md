---
description: Записывает ПУСТую запись в указанную базу данных.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: Функция Сдбвритенуллтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 363f137ecc7887114040bac76607438e0b0bfd4dbf4f3e74659c98c0906164a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815084"
---
# <a name="sdbwritenulltag-function"></a>Функция Сдбвритенуллтаг

Записывает **пустую** запись в указанную базу данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*ттаг* \[ окне\]
</dt> <dd>

ТЕГ для записи. Этот тег должен иметь тип **тега \_ \_ null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбвритебинаритаг**](sdbwritebinarytag.md)
</dt> <dt>

[**сдбвритедвордтаг**](sdbwritedwordtag.md)
</dt> <dt>

[**сдбвритестрингтаг**](sdbwritestringtag.md)
</dt> <dt>

[**сдбвритевордтаг**](sdbwritewordtag.md)
</dt> </dl>

 

 




