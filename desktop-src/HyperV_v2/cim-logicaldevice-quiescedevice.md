---
description: Метод Куиесцедевице является устаревшим вместо более общего метода RequestStateChange, который непосредственно пересекается с функциями, предоставляемыми этим методом.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Метод Куиесцедевице класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347805"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="91357-103">Метод Куиесцедевице \_ класса CIM</span><span class="sxs-lookup"><span data-stu-id="91357-103">QuiesceDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="91357-104">Метод **куиесцедевице** является устаревшим вместо более общего метода **RequestStateChange** , который непосредственно пересекается с функциями, предоставляемыми этим методом.</span><span class="sxs-lookup"><span data-stu-id="91357-104">The **QuiesceDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91357-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91357-105">Syntax</span></span>


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a><span data-ttu-id="91357-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91357-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91357-107">*Замораживание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91357-107">*Quiesce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-108">Если задано значение **true** , то все действия, выполняемые в случае **ложной** операции возобновления, прекращают работу.</span><span class="sxs-lookup"><span data-stu-id="91357-108">If set to **TRUE** then cleanly cease all activity, if **FALSE** resume activity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91357-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91357-109">Return value</span></span>

<span data-ttu-id="91357-110">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="91357-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="91357-111">Требования</span><span class="sxs-lookup"><span data-stu-id="91357-111">Requirements</span></span>



| <span data-ttu-id="91357-112">Требование</span><span class="sxs-lookup"><span data-stu-id="91357-112">Requirement</span></span> | <span data-ttu-id="91357-113">Значение</span><span class="sxs-lookup"><span data-stu-id="91357-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91357-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91357-114">Minimum supported client</span></span><br/> | <span data-ttu-id="91357-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="91357-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="91357-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91357-116">Minimum supported server</span></span><br/> | <span data-ttu-id="91357-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="91357-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="91357-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="91357-118">Namespace</span></span><br/>                | <span data-ttu-id="91357-119">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="91357-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="91357-120">MOF</span><span class="sxs-lookup"><span data-stu-id="91357-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91357-121"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91357-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="91357-122">DLL</span><span class="sxs-lookup"><span data-stu-id="91357-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91357-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="91357-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="91357-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91357-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91357-125">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="91357-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




