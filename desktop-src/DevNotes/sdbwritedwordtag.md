---
description: Записывает значение DWORD в указанную базу данных.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: Функция Сдбвритедвордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 730d171f964205638b44d5676e39abc20fb40426f7721fa6a5060d80c58805a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044794"
---
# <a name="sdbwritedwordtag-function"></a>Функция Сдбвритедвордтаг

Записывает значение **DWORD** в указанную базу данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
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

ТЕГ для записи. Этот тег должен иметь тип **тега \_ \_ DWORD**.

</dd> <dt>

*двдата* \[ окне\]
</dt> <dd>

Значение.

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

[**сдбвритеквордтаг**](sdbwriteqwordtag.md)
</dt> <dt>

[**сдбвритестрингтаг**](sdbwritestringtag.md)
</dt> <dt>

[**сдбвритевордтаг**](sdbwritewordtag.md)
</dt> </dl>

 

 




