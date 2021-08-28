---
title: Итссбтаржет, свойство TargetName
description: Указывает или получает имя целевого объекта.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Свойство TargetName службы удаленных рабочих столов
- Свойство TargetName службы удаленных рабочих столов, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство TargetName
- Свойство TargetName службы удаленных рабочих столов, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971ae66d162464c49d7eb4206f1fbddf206707c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467871"
---
# <a name="itssbtargettargetname-property"></a>Свойство Итссбтаржет:: TargetName

Указывает или получает имя целевого объекта.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Переменная **BSTR** , указывающая целевое имя.

## <a name="remarks"></a>Комментарии

Это свойство было доступно только для чтения до Windows Server 2012.

## <a name="requirements"></a>Требования




| | | Минимальный поддерживаемый клиент<br /> | Нет поддерживаемых<br /> | | Минимальный поддерживаемый сервер<br /> | Windows Server 2012<br /> | | IDL<br /> | <dl><dt>Сбтсв. idl</dt></dl> | | IID<br /> | IID_ITsSbTarget определяется следующим образом:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 на сервере Windows 2008 R2</li></ul> | 




## <a name="see-also"></a>См. также

<dl> <dt>

[**итссбтаржетекс**](itssbtargetex.md)
</dt> <dt>

[**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





