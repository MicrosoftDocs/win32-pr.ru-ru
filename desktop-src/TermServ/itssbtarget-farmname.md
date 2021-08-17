---
title: Итссбтаржет Фармнаме, свойство
description: Возвращает или задает имя фермы, к которой присоединен этот целевой объект.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Фармнаме
- Службы удаленных рабочих столов свойства Фармнаме, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство Фармнаме
- Службы удаленных рабочих столов свойства Фармнаме, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство Фармнаме
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fecf452bd6f879773a3fe200f721afbda5d29f1c41ae816846c261608d38ddca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138297"
---
# <a name="itssbtargetfarmname-property"></a>Свойство Итссбтаржет:: Фармнаме

Возвращает или задает имя фермы, к которой присоединен этот целевой объект.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Переменная **BSTR** , содержащая имя фермы.

## <a name="requirements"></a>Требования



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Минимальная версия клиента<br/></td>
<td>Ни одна версия не поддерживается<br/></td>
</tr>
<tr class="even">
<td>Минимальная версия сервера<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>IDL<br/></td>
<td><dl> <dt>Сбтсв. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget определяется следующим образом:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 на сервере Windows 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбтаржетекс**](itssbtargetex.md)
</dt> <dt>

[**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





