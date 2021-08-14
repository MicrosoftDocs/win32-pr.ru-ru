---
title: Метод Ексекутеккк класса MSAD_DomainController
description: Вызывает функцию Дсрепликаконсистенцичекк, которая вызывает средство проверки согласованности знаний (KCC) для проверки топологии репликации.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory метода Ексекутеккк
- Active Directory метода Ексекутеккк, класс MSAD_DomainController
- Класс MSAD_DomainController Active Directory, метод Ексекутеккк
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48295638f105b79ea24a55965ca3ec75ee0ad6b9982c74664f8bfecdd0681cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189625"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Метод Ексекутеккк \_ класса DOMAINCONTROLLER МСАД

Вызывает функцию [**дсрепликаконсистенцичекк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , которая вызывает средство проверки согласованности знаний (KCC) для проверки топологии репликации.

## <a name="syntax"></a>Синтаксис


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*TaskId* \[ окне\]
</dt> <dd>

Задача, которую должно выполнить KCC. **Службы каталогов \_ В настоящее время поддерживается только \_ \_ \_ топология обновления KCC TASKID** .

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Набор флагов, изменяющих поведение метода **ексекутеккк** . Этот параметр может иметь значение 0 или быть сочетанием одного или нескольких из следующих значений.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**\_флаг проверки согласованности DS, \_ \_ асинхронная \_ операция**


</dt> <dd>

Задача помещается в очередь, а затем функция возвращается, не дожидаясь завершения задачи.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_флаг проверки согласованности DS в \_ \_ клапане**


</dt> <dd>

Задача не будет добавлена в очередь, если в ближайшее время будет запущена другая задача из очереди.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**МСАДный \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





