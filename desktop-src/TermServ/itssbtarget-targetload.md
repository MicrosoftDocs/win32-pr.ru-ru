---
title: Итссбтаржет Таржетлоад, свойство
description: Извлекает относительную нагрузку на целевой объект.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Таржетлоад
- Службы удаленных рабочих столов свойства Таржетлоад, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство Таржетлоад
- Службы удаленных рабочих столов свойства Таржетлоад, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство Таржетлоад
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8224106fad6031a18bf061020a259813db639e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983927"
---
# <a name="itssbtargettargetload-property"></a>Свойство Итссбтаржет:: Таржетлоад

Извлекает относительную нагрузку на целевой объект. Это значение основано на количестве существующих и ожидающих сеансов. По умолчанию ожидающий сеанс имеет то же значение, что и существующий сеанс.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Значение свойства

Число, представляющее относительную нагрузку на целевой объект.

## <a name="remarks"></a>Комментарии

Вес ожидающего сеанса относительно активного сеанса можно изменить, задав значение параметра *\_ коннектионестаблишментпеналти балансировки нагрузки* для брокера подключений. Этот параметр находится в разделе реестра **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** . Значение по умолчанию 1 указывает, что ожидающие сеансы имеют тот же вес, что и активные сеансы.

это свойство доступно в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбтаржетекс**](itssbtargetex.md) .

## <a name="requirements"></a>Требования




| Требование | Применение |
|--------|-------|
| Минимальная версия клиента<br /> | Ни одна версия не поддерживается<br /> | 
| Минимальная версия сервера<br /> | Windows Server 2016<br /> | 
| IDL<br /> | <dl><dt>Сбтсв. idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget определяется следующим образом:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 на сервере Windows 2008 R2</li></ul> | 




## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбтаржетекс**](itssbtargetex.md)
</dt> <dt>

[**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





