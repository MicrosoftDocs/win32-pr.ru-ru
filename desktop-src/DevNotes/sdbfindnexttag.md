---
description: Выполняет поиск следующего ТЕГА в указанном родителе и возвращает TAGID совпадения.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Функция Сдбфинднексттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: fe9b9914ed9126a364fb377adc4afae84784df156a8e75c3d0d2f997f6185811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103704"
---
# <a name="sdbfindnexttag-function"></a>Функция Сдбфинднексттаг

Выполняет поиск следующего ТЕГА в указанном родителе и возвращает **TAGID** совпадения.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*типарент* \[ окне\]
</dt> <dd>

**TAGID** начала поиска. Этот параметр может иметь **тип TAGID \_ root** или **Tag \_ \_**.

</dd> <dt>

*типрев* \[ окне\]
</dt> <dd>

**TAGID** предыдущего совпадения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** совпадения.

## <a name="remarks"></a>Remarks

Перед вызовом этой функции вызовите функцию [**сдбфиндфирсттаг**](sdbfindfirsttag.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбфиндфирсттаг**](sdbfindfirsttag.md)
</dt> <dt>

[**сдбтагрефтотагид**](sdbtagreftotagid.md)
</dt> </dl>

 

 




