---
description: Блокирует и разблокирует носитель в устройстве, доступном для перемещения.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Метод Локкмедиа класса CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081679"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="ffed3-103">Метод Локкмедиа \_ класса CIM медиаакцессдевице</span><span class="sxs-lookup"><span data-stu-id="ffed3-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="ffed3-104">Блокирует и разблокирует носитель в устройстве, доступном для перемещения.</span><span class="sxs-lookup"><span data-stu-id="ffed3-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffed3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffed3-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="ffed3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffed3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffed3-107">*Блокировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffed3-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffed3-108">Если **значение — true**, блокирует носитель.</span><span class="sxs-lookup"><span data-stu-id="ffed3-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="ffed3-109">Если **значение равно false**, освобождает носитель.</span><span class="sxs-lookup"><span data-stu-id="ffed3-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffed3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffed3-110">Return value</span></span>

<span data-ttu-id="ffed3-111">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ffed3-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffed3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ffed3-112">Requirements</span></span>



| <span data-ttu-id="ffed3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ffed3-113">Requirement</span></span> | <span data-ttu-id="ffed3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ffed3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffed3-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffed3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ffed3-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffed3-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ffed3-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffed3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ffed3-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ffed3-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ffed3-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffed3-119">Namespace</span></span><br/>                | <span data-ttu-id="ffed3-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ffed3-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffed3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ffed3-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffed3-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffed3-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffed3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ffed3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffed3-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffed3-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffed3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffed3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffed3-126">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ffed3-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




