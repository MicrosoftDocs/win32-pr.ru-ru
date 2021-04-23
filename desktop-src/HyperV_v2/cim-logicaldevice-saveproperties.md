---
description: Запрашивает, что устройство захватывает текущую конфигурацию, настройки и/или сведения о состоянии в резервном хранилище.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Метод Савепропертиес класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684361"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="c90c4-103">Метод Савепропертиес \_ класса CIM</span><span class="sxs-lookup"><span data-stu-id="c90c4-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="c90c4-104">Запрашивает, что устройство захватывает текущую конфигурацию, настройки и/или сведения о состоянии в резервном хранилище.</span><span class="sxs-lookup"><span data-stu-id="c90c4-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="c90c4-105">Цель — использовать эти сведения позже (с помощью метода Ресторепропертиес), чтобы вернуть устройство к текущему условию.</span><span class="sxs-lookup"><span data-stu-id="c90c4-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="c90c4-106">Этот метод может не поддерживаться всеми устройствами.</span><span class="sxs-lookup"><span data-stu-id="c90c4-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="c90c4-107">Метод должен возвращать 0 в случае успеха, 1, если запрос не поддерживается, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="c90c4-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="c90c4-108">В подклассе можно указать набор возможных кодов возврата, используя квалификатор ValueMap в методе.</span><span class="sxs-lookup"><span data-stu-id="c90c4-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="c90c4-109">Строки, в которые содержимое ValueMap является переведенными, могут также быть указаны в подклассе как квалификатор массива Values.</span><span class="sxs-lookup"><span data-stu-id="c90c4-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="c90c4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c90c4-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="c90c4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c90c4-111">Parameters</span></span>

<span data-ttu-id="c90c4-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c90c4-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c90c4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c90c4-113">Return value</span></span>

<span data-ttu-id="c90c4-114">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c90c4-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c90c4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c90c4-115">Requirements</span></span>



| <span data-ttu-id="c90c4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c90c4-116">Requirement</span></span> | <span data-ttu-id="c90c4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c90c4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c90c4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c90c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c90c4-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c90c4-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c90c4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c90c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c90c4-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c90c4-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c90c4-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c90c4-122">Namespace</span></span><br/>                | <span data-ttu-id="c90c4-123">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c90c4-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c90c4-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c90c4-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c90c4-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c90c4-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c90c4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c90c4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c90c4-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c90c4-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c90c4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c90c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90c4-129">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="c90c4-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




