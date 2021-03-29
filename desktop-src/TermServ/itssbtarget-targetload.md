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
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784119"
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

Это свойство доступно в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбтаржетекс**](itssbtargetex.md) .

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
<td>Windows Server 2016<br/></td>
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
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 на Windows Server 2008 R2</li>
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

 

 





