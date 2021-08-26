---
description: Высвобождает ресурсы, используемые функцией Сдбжетматчинжексе.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Функция Сдбрелеасематчинжексе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 710874fc0e57775eb6ad1c9c6681a5b74dc66d133b22ce23d2ac0d27270ef7f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044924"
---
# <a name="sdbreleasematchingexe-function"></a>Функция Сдбрелеасематчинжексе

Высвобождает ресурсы, используемые функцией [**сдбжетматчинжексе**](sdbgetmatchingexe.md) .

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсдб* \[ окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .

</dd> <dt>

*трексе* \[ окне\]
</dt> <dd>

[**Тагреф**](tagref.md) , возвращенный [**сдбжетматчинжексе**](sdbgetmatchingexe.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбжетматчинжексе**](sdbgetmatchingexe.md)
</dt> <dt>

[**сдбинитдатабасе**](sdbinitdatabase.md)
</dt> </dl>

 

 




