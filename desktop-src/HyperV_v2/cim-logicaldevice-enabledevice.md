---
description: Метод Енабледевице является устаревшим вместо более общего метода RequestStateChange, который непосредственно пересекается с функциями, предоставляемыми этим методом.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Метод Енабледевице класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663747"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="d4ef0-103">Метод Енабледевице \_ класса CIM</span><span class="sxs-lookup"><span data-stu-id="d4ef0-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="d4ef0-104">Метод Енабледевице является устаревшим вместо более общего метода RequestStateChange, который непосредственно пересекается с функциями, предоставляемыми этим методом.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="d4ef0-105">Запрашивает включение объектного ключа ("Enabled", "input Parameter = TRUE") или Disabled (= FALSE).</span><span class="sxs-lookup"><span data-stu-id="d4ef0-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="d4ef0-106">В случае успешного выполнения свойства Статусинфо/EnabledState устройства должны отражать требуемое состояние (включено/отключено).</span><span class="sxs-lookup"><span data-stu-id="d4ef0-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="d4ef0-107">Обратите внимание, что функция этого метода пересекается со свойством RequestedState.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="d4ef0-108">Объект RequestedState был добавлен в модель для обслуживания записи (т. е. сохраненного значения) последнего запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="d4ef0-109">При вызове метода Енабледевице должно быть задано свойство RequestedState соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="d4ef0-110">Код возврата должен быть равен 0, если запрос был успешно выполнен, 1, если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="d4ef0-111">В подклассе можно указать набор возможных кодов возврата, используя квалификатор ValueMap в методе.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="d4ef0-112">Строки, в которые содержимое ValueMap является переведенными, могут также быть указаны в подклассе как квалификатор массива Values.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ef0-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4ef0-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="d4ef0-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4ef0-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ef0-115">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4ef0-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ef0-116">Если значение TRUE, включите устройство, если значение равно FALSE, отключите устройство.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ef0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4ef0-117">Return value</span></span>

<span data-ttu-id="d4ef0-118">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d4ef0-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ef0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d4ef0-119">Requirements</span></span>



| <span data-ttu-id="d4ef0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d4ef0-120">Requirement</span></span> | <span data-ttu-id="d4ef0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ef0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ef0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4ef0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ef0-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d4ef0-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d4ef0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4ef0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ef0-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d4ef0-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d4ef0-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4ef0-126">Namespace</span></span><br/>                | <span data-ttu-id="d4ef0-127">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d4ef0-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d4ef0-128">MOF</span><span class="sxs-lookup"><span data-stu-id="d4ef0-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4ef0-129"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4ef0-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4ef0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ef0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ef0-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4ef0-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d4ef0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4ef0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ef0-133">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="d4ef0-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




