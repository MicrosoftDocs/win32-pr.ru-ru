---
description: Начинает выполнение задачи.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Метод Тасккомплетионклиент:: Апплитасккомплетион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 58c95144077697f1655547a58571ce3475355aa96040ce1815bd3178bc9a1290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773674"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>Метод Тасккомплетионклиент:: Апплитасккомплетион

Начинает выполнение задачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пткфкатегори* 
</dt> <dd>

Значение, указывающее категорию задачи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Единственным поддерживаемым значением для *пткфкатегори* является 0x08000000.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**тасккомплетионклиент**](taskcompletionclient.md)
</dt> </dl>

 

 




