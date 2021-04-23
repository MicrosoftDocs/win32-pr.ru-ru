---
title: IMsRdpClientShell2 Секуредсеттингсенаблед, свойство
description: Получает значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClientShell2
- Службы удаленных рабочих столов интерфейса IMsRdpClientShell2, свойство Секуредсеттингсенаблед
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672836"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="e7b3e-106">Свойство IMsRdpClientShell2:: Секуредсеттингсенаблед</span><span class="sxs-lookup"><span data-stu-id="e7b3e-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="e7b3e-107">Получает значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e7b3e-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="e7b3e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e7b3e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b3e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7b3e-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="e7b3e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e7b3e-110">Property value</span></span>

<span data-ttu-id="e7b3e-111">Указатель на логическое значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e7b3e-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b3e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e7b3e-112">Requirements</span></span>



| <span data-ttu-id="e7b3e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e7b3e-113">Requirement</span></span> | <span data-ttu-id="e7b3e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e7b3e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b3e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7b3e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b3e-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7b3e-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e7b3e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7b3e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b3e-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7b3e-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="e7b3e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e7b3e-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7b3e-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7b3e-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b3e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7b3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b3e-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="e7b3e-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





