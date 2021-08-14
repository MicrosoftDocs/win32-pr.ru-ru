---
title: Итссбресаурцеплугинсторикс Релеасетаржетлокк, метод
description: Снимает блокировку на целевой объект.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Релеасетаржетлокк
- Службы удаленных рабочих столов метода Релеасетаржетлокк, интерфейс Итссбресаурцеплугинсторикс
- Службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс, метод Релеасетаржетлокк
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fbe40d0fc7a28697d0e2fa9727f9e844eb39759db0dddf02c1d9e01bd843c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989914"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>Метод Итссбресаурцеплугинсторикс:: Релеасетаржетлокк

Снимает блокировку на целевой объект.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекст* \[ окне\]
</dt> <dd>

Указатель на контекст, возвращенный методом [**аккуиретаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

этот метод доступен только в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбресаурцеплугинсторикс**](itssbresourcepluginstoreex.md) . Этот метод доступен в интерфейсе [**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) , начиная с Windows Server 2016.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                             |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                             |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl>          |
| IID<br/>                      | IID \_ итссбресаурцеплугинсторикс определен как 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбресаурцеплугинсторикс**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





