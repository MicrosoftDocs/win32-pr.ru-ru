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
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="ca74d-111">Свойство Итссбтаржет:: IpAddresses</span><span class="sxs-lookup"><span data-stu-id="ca74d-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="ca74d-112">Возвращает или задает внешние IP-адреса целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ca74d-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="ca74d-113">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ca74d-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca74d-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca74d-114">Syntax</span></span>


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



## <a name="property-value"></a><span data-ttu-id="ca74d-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ca74d-115">Property value</span></span>

<span data-ttu-id="ca74d-116">Указатель на массив структур [**тссд \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) , которые получают внешние IP-адреса целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ca74d-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="ca74d-117">Указатель на переменную **типа DWORD** , которая содержит количество внешних IP-адресов в параметре *SOCKADDR* .</span><span class="sxs-lookup"><span data-stu-id="ca74d-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="ca74d-118">Если число адресов неизвестно, передайте *SOCKADDR* как **null**.</span><span class="sxs-lookup"><span data-stu-id="ca74d-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="ca74d-119">Метод возвратит число структур [**тссд \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) , необходимых для выделения в массиве, на который указывает параметр *SOCKADDR* .</span><span class="sxs-lookup"><span data-stu-id="ca74d-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca74d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca74d-120">Remarks</span></span>

<span data-ttu-id="ca74d-121">Это свойство ранее называлось **таржетекстерналипаддрессес** в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ca74d-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="ca74d-122">Если число внешних IP-адресов неизвестно, можно вызвать этот метод с параметром *SOCKADDR* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ca74d-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="ca74d-123">Затем метод возвратит в параметре *нумаддрессес* количество структур [**тссд \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) , необходимых для получения всех внешних IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ca74d-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="ca74d-124">Выделите массив для *SOCKADDR* на основе этого числа, а затем снова вызовите метод, установив для *SOCKADDR* только что выделенный массив и *нумаддрессес* в число, возвращенное первым вызовом.</span><span class="sxs-lookup"><span data-stu-id="ca74d-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca74d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ca74d-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca74d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca74d-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="ca74d-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca74d-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca74d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca74d-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="ca74d-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca74d-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca74d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="ca74d-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="ca74d-131"><dt>Сбтсв. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="ca74d-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca74d-132">IID</span><span class="sxs-lookup"><span data-stu-id="ca74d-132">IID</span></span><br/></td>
<td><span data-ttu-id="ca74d-133">IID_ITsSbTarget определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ca74d-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="ca74d-134">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="ca74d-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="ca74d-135">e85e10ea-db0b-4752-b456-5fd5840901c0 на Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca74d-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="ca74d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca74d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca74d-137">**итссбтаржетекс**</span><span class="sxs-lookup"><span data-stu-id="ca74d-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="ca74d-138">**итссбтаржет**</span><span class="sxs-lookup"><span data-stu-id="ca74d-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="ca74d-139">**ТССД \_ ConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="ca74d-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





