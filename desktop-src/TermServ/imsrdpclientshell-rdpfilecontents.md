---
title: Имсрдпклиентшелл Рдпфилеконтентс, свойство
description: Указывает или получает содержимое файла протокол удаленного рабочего стола (RDP) для запуска из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или с другого веб-портала.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Рдпфилеконтентс
- Службы удаленных рабочих столов свойства Рдпфилеконтентс, интерфейс Имсрдпклиентшелл
- Службы удаленных рабочих столов интерфейса Имсрдпклиентшелл, свойство Рдпфилеконтентс
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681974"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="24c54-106">Свойство Имсрдпклиентшелл:: Рдпфилеконтентс</span><span class="sxs-lookup"><span data-stu-id="24c54-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="24c54-107">Указывает или получает содержимое файла протокол удаленного рабочего стола (RDP) для запуска из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или с другого веб-портала.</span><span class="sxs-lookup"><span data-stu-id="24c54-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="24c54-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="24c54-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c54-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24c54-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="24c54-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="24c54-110">Property value</span></span>

<span data-ttu-id="24c54-111">Указывает содержимое RDP-файла, которое должно быть запущено с портала.</span><span class="sxs-lookup"><span data-stu-id="24c54-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c54-112">Требования</span><span class="sxs-lookup"><span data-stu-id="24c54-112">Requirements</span></span>



| <span data-ttu-id="24c54-113">Требование</span><span class="sxs-lookup"><span data-stu-id="24c54-113">Requirement</span></span> | <span data-ttu-id="24c54-114">Значение</span><span class="sxs-lookup"><span data-stu-id="24c54-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24c54-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24c54-115">Minimum supported client</span></span><br/> | <span data-ttu-id="24c54-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24c54-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="24c54-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24c54-117">Minimum supported server</span></span><br/> | <span data-ttu-id="24c54-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24c54-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="24c54-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="24c54-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="24c54-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24c54-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="24c54-121">DLL</span><span class="sxs-lookup"><span data-stu-id="24c54-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24c54-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24c54-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="24c54-123">IID</span><span class="sxs-lookup"><span data-stu-id="24c54-123">IID</span></span><br/>                      | <span data-ttu-id="24c54-124">IID \_ имсрдпклиентшелл определен как d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="24c54-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="24c54-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24c54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c54-126">**имсрдпклиентшелл**</span><span class="sxs-lookup"><span data-stu-id="24c54-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





