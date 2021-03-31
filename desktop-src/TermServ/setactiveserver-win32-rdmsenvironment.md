---
title: Метод Сетактивесервер класса Win32_RDMSEnvironment
description: Задает полное доменное имя среды службы управления удаленный рабочий стол (RDMS) для текущего узла.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетактивесервер
- Службы удаленных рабочих столов метода Сетактивесервер, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Сетактивесервер
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490311"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="37500-106">Метод Сетактивесервер \_ класса Win32 рдмсенвиронмент</span><span class="sxs-lookup"><span data-stu-id="37500-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="37500-107">Задает полное доменное имя среды службы управления удаленный рабочий стол (RDMS) для текущего узла.</span><span class="sxs-lookup"><span data-stu-id="37500-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="37500-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37500-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="37500-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="37500-109">Parameters</span></span>

<span data-ttu-id="37500-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="37500-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37500-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37500-111">Return value</span></span>

<span data-ttu-id="37500-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="37500-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="37500-113">Требования</span><span class="sxs-lookup"><span data-stu-id="37500-113">Requirements</span></span>



| <span data-ttu-id="37500-114">Требование</span><span class="sxs-lookup"><span data-stu-id="37500-114">Requirement</span></span> | <span data-ttu-id="37500-115">Значение</span><span class="sxs-lookup"><span data-stu-id="37500-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="37500-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37500-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37500-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="37500-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="37500-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37500-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37500-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37500-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="37500-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37500-120">Namespace</span></span><br/>                | <span data-ttu-id="37500-121">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="37500-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="37500-122">MOF</span><span class="sxs-lookup"><span data-stu-id="37500-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37500-123"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37500-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="37500-124">DLL</span><span class="sxs-lookup"><span data-stu-id="37500-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37500-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37500-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="37500-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37500-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37500-127">**\_Рдмсенвиронмент Win32**</span><span class="sxs-lookup"><span data-stu-id="37500-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





