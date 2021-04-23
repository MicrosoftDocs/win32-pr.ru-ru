---
description: Отключает сетевой адаптер.
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Метод Disable класса Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655806"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="fa514-103">Метод Disable \_ класса Win32 сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="fa514-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="fa514-104">Метод **Disable** отключает сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="fa514-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa514-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa514-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="fa514-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa514-106">Parameters</span></span>

<span data-ttu-id="fa514-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fa514-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa514-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa514-108">Return value</span></span>

<span data-ttu-id="fa514-109">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="fa514-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="fa514-110">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="fa514-110">Any other number indicates an error.</span></span> <span data-ttu-id="fa514-111">Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fa514-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa514-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fa514-112">Requirements</span></span>



| <span data-ttu-id="fa514-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fa514-113">Requirement</span></span> | <span data-ttu-id="fa514-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fa514-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa514-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa514-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fa514-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa514-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa514-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa514-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fa514-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa514-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa514-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fa514-119">Namespace</span></span><br/>                | <span data-ttu-id="fa514-120">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fa514-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa514-121">MOF</span><span class="sxs-lookup"><span data-stu-id="fa514-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa514-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa514-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa514-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fa514-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa514-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa514-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa514-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa514-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa514-126">**\_Сетевого адаптера Win32**</span><span class="sxs-lookup"><span data-stu-id="fa514-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="fa514-127">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="fa514-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="fa514-128">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="fa514-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

