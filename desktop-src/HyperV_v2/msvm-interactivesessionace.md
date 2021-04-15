---
description: Представляет запись управления доступом (ACE), определяющую доступ к интерактивному сеансу виртуальной машины.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Класс Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682841"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="1844d-103">\_Класс мсвм интерактивесессионаце</span><span class="sxs-lookup"><span data-stu-id="1844d-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="1844d-104">Представляет *запись управления доступом* (ACE), определяющую доступ к интерактивному сеансу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1844d-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="1844d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1844d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1844d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1844d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="1844d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1844d-107">Members</span></span>

<span data-ttu-id="1844d-108">Класс **мсвм \_ интерактивесессионаце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1844d-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="1844d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1844d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1844d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1844d-110">Properties</span></span>

<span data-ttu-id="1844d-111">Класс **мсвм \_ интерактивесессионаце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1844d-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1844d-112">**акцесстипе**</span><span class="sxs-lookup"><span data-stu-id="1844d-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1844d-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1844d-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1844d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1844d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1844d-115">Указывает, предоставляет ли ACE или запрещает доступ к доверенному лицу.</span><span class="sxs-lookup"><span data-stu-id="1844d-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="1844d-116">**Доступ разрешен** (0)</span><span class="sxs-lookup"><span data-stu-id="1844d-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="1844d-117">**Отказано в доступе** (1)</span><span class="sxs-lookup"><span data-stu-id="1844d-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1844d-118">**Доверенное лицо**</span><span class="sxs-lookup"><span data-stu-id="1844d-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1844d-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1844d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1844d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1844d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1844d-121">Определяет субъект безопасности, к которому ACE предоставляет или запрещает доступ.</span><span class="sxs-lookup"><span data-stu-id="1844d-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="1844d-122">Допустимые форматы для этого свойства включают формат имени пользователя, совместимый с Windows SAM, и формат строки идентификатора безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="1844d-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1844d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1844d-123">Requirements</span></span>



| <span data-ttu-id="1844d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1844d-124">Requirement</span></span> | <span data-ttu-id="1844d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1844d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1844d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1844d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1844d-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1844d-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1844d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1844d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1844d-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1844d-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1844d-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1844d-130">Namespace</span></span><br/>                | <span data-ttu-id="1844d-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1844d-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1844d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1844d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1844d-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1844d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1844d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1844d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1844d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1844d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1844d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1844d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1844d-137">**жетинтерактивесессионакл**</span><span class="sxs-lookup"><span data-stu-id="1844d-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




