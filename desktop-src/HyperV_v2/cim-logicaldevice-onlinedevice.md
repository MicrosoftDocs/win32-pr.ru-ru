---
description: Метод Онлинедевице является устаревшим вместо более общего метода RequestStateChange, который непосредственно пересекается с функциями, предоставляемыми этим методом.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Метод Онлинедевице класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684283"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="d36dc-103">Метод Онлинедевице \_ класса CIM</span><span class="sxs-lookup"><span data-stu-id="d36dc-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="d36dc-104">Метод **онлинедевице** является устаревшим вместо более общего метода **RequestStateChange** , который непосредственно пересекается с функциями, предоставляемыми этим методом.</span><span class="sxs-lookup"><span data-stu-id="d36dc-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d36dc-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="d36dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d36dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36dc-107">В *сети* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d36dc-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d36dc-108">Если **значение — true**, переведите устройство в режим «в сети», если **значение false**, перевести устройство в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="d36dc-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36dc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d36dc-109">Return value</span></span>

<span data-ttu-id="d36dc-110">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d36dc-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d36dc-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d36dc-111">Requirements</span></span>



| <span data-ttu-id="d36dc-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d36dc-112">Requirement</span></span> | <span data-ttu-id="d36dc-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d36dc-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d36dc-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d36dc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d36dc-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d36dc-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d36dc-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d36dc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d36dc-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d36dc-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d36dc-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d36dc-118">Namespace</span></span><br/>                | <span data-ttu-id="d36dc-119">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d36dc-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d36dc-120">MOF</span><span class="sxs-lookup"><span data-stu-id="d36dc-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d36dc-121"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d36dc-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d36dc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d36dc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d36dc-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d36dc-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d36dc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d36dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36dc-125">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="d36dc-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




