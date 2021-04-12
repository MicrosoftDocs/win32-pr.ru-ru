---
description: Запрашивает сброс объекта типа "логическое".
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Метод Reset класса CIM_LogicalDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347795"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="d6dcc-103">Метод Reset класса CIM_LogicalDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d6dcc-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="d6dcc-104">Запрашивает сброс объекта типа "логическое".</span><span class="sxs-lookup"><span data-stu-id="d6dcc-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="d6dcc-105">В подклассе можно указать набор возможных кодов возврата, используя квалификатор ValueMap в методе.</span><span class="sxs-lookup"><span data-stu-id="d6dcc-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="d6dcc-106">Строки, в которые содержимое ValueMap является переведенными, могут также быть указаны в подклассе как квалификатор массива Values.</span><span class="sxs-lookup"><span data-stu-id="d6dcc-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dcc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6dcc-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="d6dcc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6dcc-108">Parameters</span></span>

<span data-ttu-id="d6dcc-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d6dcc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6dcc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6dcc-110">Return value</span></span>

<span data-ttu-id="d6dcc-111">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d6dcc-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dcc-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d6dcc-112">Requirements</span></span>



| <span data-ttu-id="d6dcc-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d6dcc-113">Requirement</span></span> | <span data-ttu-id="d6dcc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d6dcc-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dcc-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6dcc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dcc-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d6dcc-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d6dcc-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6dcc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dcc-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d6dcc-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d6dcc-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d6dcc-119">Namespace</span></span><br/>                | <span data-ttu-id="d6dcc-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d6dcc-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d6dcc-121">MOF</span><span class="sxs-lookup"><span data-stu-id="d6dcc-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6dcc-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcc-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6dcc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d6dcc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6dcc-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcc-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d6dcc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6dcc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dcc-126">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="d6dcc-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




