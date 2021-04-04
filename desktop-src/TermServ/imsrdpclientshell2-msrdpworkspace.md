---
title: IMsRdpClientShell2 Мсрдпворкспаце, свойство
description: Получает указатель на интерфейс Имсрдпворкспаце, используемый для управления учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Мсрдпворкспаце
- Службы удаленных рабочих столов свойства Мсрдпворкспаце, интерфейс IMsRdpClientShell2
- Службы удаленных рабочих столов интерфейса IMsRdpClientShell2, свойство Мсрдпворкспаце
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802950"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="59756-106">Свойство IMsRdpClientShell2:: Мсрдпворкспаце</span><span class="sxs-lookup"><span data-stu-id="59756-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="59756-107">Получает указатель на интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) , используемый для управления учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="59756-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="59756-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="59756-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59756-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59756-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="59756-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="59756-110">Property value</span></span>

<span data-ttu-id="59756-111">Адрес указателя на интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) .</span><span class="sxs-lookup"><span data-stu-id="59756-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="59756-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59756-112">Remarks</span></span>

<span data-ttu-id="59756-113">Интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) не предоставляется как пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="59756-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="59756-114">Доступ к нему возможен только через методы [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="59756-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="59756-115">Требования</span><span class="sxs-lookup"><span data-stu-id="59756-115">Requirements</span></span>



| <span data-ttu-id="59756-116">Требование</span><span class="sxs-lookup"><span data-stu-id="59756-116">Requirement</span></span> | <span data-ttu-id="59756-117">Значение</span><span class="sxs-lookup"><span data-stu-id="59756-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59756-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59756-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59756-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59756-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59756-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59756-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59756-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59756-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="59756-122">DLL</span><span class="sxs-lookup"><span data-stu-id="59756-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59756-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59756-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59756-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59756-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59756-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="59756-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

