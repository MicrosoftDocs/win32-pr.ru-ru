---
title: Метод logoff класса Win32_VirtualDesktopSession (Сенсевтс. h)
description: Выполнит выход пользователя из сеанса виртуального рабочего стола.
ms.assetid: a9c90ace-324c-4eec-86e1-30ce35307e52
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода выхода
- Метод выхода из службы удаленных рабочих столов, Win32_VirtualDesktopSession класс
- Службы удаленных рабочих столов класса Win32_VirtualDesktopSession, метод logoff
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Logoff
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4582744f0d8ba9300bd620a45190ec1de4819ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415845"
---
# <a name="logoff-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="72d4a-106">Метод logoff \_ класса Win32 виртуалдесктопсессион</span><span class="sxs-lookup"><span data-stu-id="72d4a-106">Logoff method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="72d4a-107">Выполнит выход пользователя из сеанса виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="72d4a-107">Logs off the user from the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d4a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72d4a-108">Syntax</span></span>


```mof
uint32 Logoff();
```



## <a name="parameters"></a><span data-ttu-id="72d4a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="72d4a-109">Parameters</span></span>

<span data-ttu-id="72d4a-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="72d4a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72d4a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72d4a-111">Return value</span></span>

<span data-ttu-id="72d4a-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="72d4a-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d4a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="72d4a-113">Requirements</span></span>



| <span data-ttu-id="72d4a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="72d4a-114">Requirement</span></span> | <span data-ttu-id="72d4a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="72d4a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d4a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72d4a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="72d4a-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="72d4a-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="72d4a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72d4a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="72d4a-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72d4a-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="72d4a-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72d4a-120">Namespace</span></span><br/>                | <span data-ttu-id="72d4a-121">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="72d4a-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="72d4a-122">Header</span><span class="sxs-lookup"><span data-stu-id="72d4a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d4a-123"><dt>Сенсевтс. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d4a-123"><dt>Sensevts.h</dt></span></span> </dl>       |
| <span data-ttu-id="72d4a-124">MOF</span><span class="sxs-lookup"><span data-stu-id="72d4a-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72d4a-125"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72d4a-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="72d4a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="72d4a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d4a-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d4a-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="72d4a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72d4a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d4a-129">**\_Виртуалдесктопсессион Win32**</span><span class="sxs-lookup"><span data-stu-id="72d4a-129">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





