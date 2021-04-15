---
title: Итссбтаржет IpAddresses, свойство
description: Возвращает или задает внешние IP-адреса целевого объекта.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Таржетекстерналипаддрессес
- Службы удаленных рабочих столов свойства Таржетекстерналипаддрессес, интерфейс Итссбтаржет
- Службы удаленных рабочих столов свойства Таржетекстерналипаддрессес, интерфейс Итссбтаржет
- службы удаленных рабочих столов свойства IpAddresses
- Службы удаленных рабочих столов свойства IpAddresses, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство IpAddresses
- Службы удаленных рабочих столов свойства IpAddresses, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство IpAddresses
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411766"
---
# <a name="itssbtargetipaddresses-property"></a>Свойство Итссбтаржет:: IpAddresses

Возвращает или задает внешние IP-адреса целевого объекта.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>Значение свойства

Указатель на массив структур [**тссд \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) , которые получают внешние IP-адреса целевого объекта.

Указатель на переменную **типа DWORD** , которая содержит количество внешних IP-адресов в параметре *SOCKADDR* . Если число адресов неизвестно, передайте *SOCKADDR* как **null**. Метод возвратит число структур [**тссд \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) , необходимых для выделения в массиве, на который указывает параметр *SOCKADDR* .

## <a name="remarks"></a>Комментарии

Это свойство ранее называлось **таржетекстерналипаддрессес** в Windows Server 2008 R2.

Если число внешних IP-адресов неизвестно, можно вызвать этот метод с параметром *SOCKADDR* , имеющим значение **null**. Затем метод возвратит в параметре *нумаддрессес* количество структур [**тссд \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) , необходимых для получения всех внешних IP-адресов. Выделите массив для *SOCKADDR* на основе этого числа, а затем снова вызовите метод, установив для *SOCKADDR* только что выделенный массив и *нумаддрессес* в число, возвращенное первым вызовом.

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
</dt> <dt>

[**ТССД \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





