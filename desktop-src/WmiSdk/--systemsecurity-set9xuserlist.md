---
description: Задает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: 'Метод __SystemSecurity:: Set9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693503"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="bc785-103">\_\_Метод Системсекурити:: Set9XUserList</span><span class="sxs-lookup"><span data-stu-id="bc785-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="bc785-104">Метод **\_ \_ системсекурити:: Set9XUserList** задает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="bc785-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="bc785-105">Список указывается в виде массива внедренных объектов, где каждый объект является экземпляром класса [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) .</span><span class="sxs-lookup"><span data-stu-id="bc785-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="bc785-106">Эта функция аналогична дескриптору безопасности, но более ограничена.</span><span class="sxs-lookup"><span data-stu-id="bc785-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="bc785-107">Группы не поддерживаются, и локальный доступ не контролируется, так как локальный пользователь всегда имеет полный доступ.</span><span class="sxs-lookup"><span data-stu-id="bc785-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="bc785-108">Разрешены и Deny, и разрешить записи контроля доступа (ACE), и поэтому порядок ACE важен в списке управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="bc785-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="bc785-109">Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="bc785-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc785-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc785-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="bc785-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc785-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc785-112">*UL* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc785-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc785-113">Массив пользователей.</span><span class="sxs-lookup"><span data-stu-id="bc785-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc785-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc785-114">Return value</span></span>

<span data-ttu-id="bc785-115">Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода.</span><span class="sxs-lookup"><span data-stu-id="bc785-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="bc785-116">В следующем списке перечислены возвращаемые значения, которые являются значимыми для **Set9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="bc785-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="bc785-117">Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bc785-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="bc785-118">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bc785-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="bc785-119">**\_метод WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="bc785-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="bc785-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bc785-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc785-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bc785-121">Requirements</span></span>



| <span data-ttu-id="bc785-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bc785-122">Requirement</span></span> | <span data-ttu-id="bc785-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bc785-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bc785-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc785-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc785-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc785-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bc785-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc785-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc785-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc785-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="bc785-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bc785-128">Namespace</span></span><br/>                | <span data-ttu-id="bc785-129">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="bc785-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bc785-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc785-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc785-131">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="bc785-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bc785-132">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="bc785-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="bc785-133">**\_\_Системсекурити:: получает**</span><span class="sxs-lookup"><span data-stu-id="bc785-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="bc785-134">**\_\_Системсекурити:: настраивается**</span><span class="sxs-lookup"><span data-stu-id="bc785-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="bc785-135">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="bc785-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="bc785-136">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="bc785-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="bc785-137">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="bc785-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="bc785-138">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="bc785-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

