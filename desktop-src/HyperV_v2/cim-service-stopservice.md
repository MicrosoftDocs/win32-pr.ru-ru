---
description: Скорость службы в остановленном состоянии.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Метод работы класса CIM_Service (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897630"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="51cf5-103">Метод работы класса CIM_Service (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="51cf5-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="51cf5-104">Скорость службы в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="51cf5-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="51cf5-105">Семантика этого метода пересекается с методом **RequestStateChange** , унаследованным от [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="51cf5-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="51cf5-106">Этот метод поддерживается, так как он широко реализован, а его простая семантика "остановлена" удобна для использования.</span><span class="sxs-lookup"><span data-stu-id="51cf5-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="51cf5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51cf5-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="51cf5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51cf5-108">Parameters</span></span>

<span data-ttu-id="51cf5-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="51cf5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51cf5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51cf5-110">Return value</span></span>

<span data-ttu-id="51cf5-111">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="51cf5-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cf5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="51cf5-112">Requirements</span></span>



| <span data-ttu-id="51cf5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="51cf5-113">Requirement</span></span> | <span data-ttu-id="51cf5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="51cf5-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51cf5-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51cf5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="51cf5-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51cf5-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="51cf5-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51cf5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="51cf5-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="51cf5-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="51cf5-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51cf5-119">Namespace</span></span><br/>                | <span data-ttu-id="51cf5-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="51cf5-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="51cf5-121">MOF</span><span class="sxs-lookup"><span data-stu-id="51cf5-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51cf5-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51cf5-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51cf5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="51cf5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51cf5-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51cf5-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51cf5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51cf5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cf5-126">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="51cf5-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




