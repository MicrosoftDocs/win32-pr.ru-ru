---
title: Метод запуска Имсрдпклиентшелл
description: Запускает содержимое удаленного файла из удаленный рабочий стол Веб-доступ (Веб-доступ удаленных рабочих столов) или с другого веб-портала.
ms.assetid: a0aa12e4-8b6f-4a3a-a6b8-f5def0b8bd90
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода запуска
- Метод запуска службы удаленных рабочих столов, интерфейс Имсрдпклиентшелл
- Службы удаленных рабочих столов интерфейса Имсрдпклиентшелл, метод Launch
topic_type:
- apiref
api_name:
- IMsRdpClientShell.Launch
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae895d8a12824c6aca1dcbd69c5055b3ca6f3e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415052"
---
# <a name="imsrdpclientshelllaunch-method"></a><span data-ttu-id="4e0a9-106">Метод Имсрдпклиентшелл:: Launch</span><span class="sxs-lookup"><span data-stu-id="4e0a9-106">IMsRdpClientShell::Launch method</span></span>

<span data-ttu-id="4e0a9-107">Запускает содержимое удаленного файла из удаленный рабочий стол Веб-доступ (Веб-доступ удаленных рабочих столов) или с другого веб-портала.</span><span class="sxs-lookup"><span data-stu-id="4e0a9-107">Launches remote file content from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0a9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e0a9-108">Syntax</span></span>


```C++
HRESULT Launch();
```



## <a name="parameters"></a><span data-ttu-id="4e0a9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e0a9-109">Parameters</span></span>

<span data-ttu-id="4e0a9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e0a9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e0a9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e0a9-111">Return value</span></span>

<span data-ttu-id="4e0a9-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4e0a9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e0a9-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e0a9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0a9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4e0a9-114">Requirements</span></span>



| <span data-ttu-id="4e0a9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4e0a9-115">Requirement</span></span> | <span data-ttu-id="4e0a9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4e0a9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0a9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e0a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0a9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e0a9-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4e0a9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e0a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0a9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e0a9-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4e0a9-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4e0a9-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e0a9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a9-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e0a9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4e0a9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e0a9-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e0a9-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e0a9-125">IID</span><span class="sxs-lookup"><span data-stu-id="4e0a9-125">IID</span></span><br/>                      | <span data-ttu-id="4e0a9-126">IID \_ имсрдпклиентшелл определен как d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="4e0a9-126">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="4e0a9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e0a9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0a9-128">**имсрдпклиентшелл**</span><span class="sxs-lookup"><span data-stu-id="4e0a9-128">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





