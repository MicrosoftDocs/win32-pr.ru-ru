---
description: Получает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: 'Метод __SystemSecurity:: Get9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656665"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="bcb5f-103">\_\_Метод Системсекурити:: Get9XUserList</span><span class="sxs-lookup"><span data-stu-id="bcb5f-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="bcb5f-104">Метод [**\_ \_ системсекурити:: Set9XUserList**](--systemsecurity-set9xuserlist.md) получает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="bcb5f-105">Эта функция аналогична дескриптору безопасности, но более ограничена.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="bcb5f-106">Группы не поддерживаются, и локальный доступ не контролируется, так как локальный пользователь всегда имеет полный доступ.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="bcb5f-107">Разрешены и Deny, и разрешить записи контроля доступа (ACE), и поэтому порядок ACE важен в списке управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="bcb5f-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="bcb5f-108">Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="bcb5f-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb5f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcb5f-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="bcb5f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcb5f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb5f-111">*UL* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bcb5f-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb5f-112">Массив пользователей.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb5f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcb5f-113">Return value</span></span>

<span data-ttu-id="bcb5f-114">Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="bcb5f-115">В следующем списке перечислены возвращаемые значения, которые являются значимыми для **Get9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="bcb5f-116">Для сценариев и Visual Basic приложений результат может быть [параметром Parameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bcb5f-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="bcb5f-117">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bcb5f-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="bcb5f-118">**\_метод WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="bcb5f-119">Этот метод не поддерживается в поддерживаемых версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcb5f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bcb5f-120">Requirements</span></span>



| <span data-ttu-id="bcb5f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bcb5f-121">Requirement</span></span> | <span data-ttu-id="bcb5f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bcb5f-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bcb5f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcb5f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb5f-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcb5f-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bcb5f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcb5f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb5f-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcb5f-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="bcb5f-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bcb5f-127">Namespace</span></span><br/>                | <span data-ttu-id="bcb5f-128">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="bcb5f-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bcb5f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcb5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb5f-130">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="bcb5f-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bcb5f-131">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="bcb5f-132">**\_\_Системсекурити:: получает**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="bcb5f-133">**\_\_Системсекурити:: настраивается**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="bcb5f-134">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="bcb5f-135">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="bcb5f-136">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="bcb5f-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="bcb5f-137">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="bcb5f-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

