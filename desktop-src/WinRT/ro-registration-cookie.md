---
description: Представляет фабрики активации, зарегистрированные путем вызова функции Рорегистерактиватионфакториес.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Роапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701570"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="c17bb-103">\_ \_ файл cookie регистрации ro</span><span class="sxs-lookup"><span data-stu-id="c17bb-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="c17bb-104">Представляет фабрики активации, зарегистрированные путем вызова функции [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .</span><span class="sxs-lookup"><span data-stu-id="c17bb-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="c17bb-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c17bb-105">Remarks</span></span>

<span data-ttu-id="c17bb-106">Функция [**рорегистерактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) возвращает **\_ \_ файл cookie регистрации ro** , если фабрики класса активируемого зарегистрированы в среда выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="c17bb-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="c17bb-107">Функция [**роревокеактиватионфакториес**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) использует файл cookie для удаления фабрик класса.</span><span class="sxs-lookup"><span data-stu-id="c17bb-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="c17bb-108">Требования</span><span class="sxs-lookup"><span data-stu-id="c17bb-108">Requirements</span></span>



| <span data-ttu-id="c17bb-109">Требование</span><span class="sxs-lookup"><span data-stu-id="c17bb-109">Requirement</span></span> | <span data-ttu-id="c17bb-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c17bb-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c17bb-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c17bb-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c17bb-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c17bb-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="c17bb-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c17bb-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c17bb-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c17bb-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="c17bb-115">Header</span><span class="sxs-lookup"><span data-stu-id="c17bb-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="c17bb-116"><dt>Роапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c17bb-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17bb-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c17bb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c17bb-118">**рорегистерактиватионфакториес**</span><span class="sxs-lookup"><span data-stu-id="c17bb-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="c17bb-119">**роревокеактиватионфакториес**</span><span class="sxs-lookup"><span data-stu-id="c17bb-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
