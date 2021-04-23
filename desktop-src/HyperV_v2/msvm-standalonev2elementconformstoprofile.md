---
description: Определяет зарегистрированные профили, на которые ссылается изолированная автономная система.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Класс Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991463"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="8549a-103">\_Класс мсвм StandaloneV2ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="8549a-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="8549a-104">Определяет зарегистрированные профили, на которые ссылается изолированная автономная система.</span><span class="sxs-lookup"><span data-stu-id="8549a-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="8549a-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8549a-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8549a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8549a-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="8549a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8549a-107">Members</span></span>

<span data-ttu-id="8549a-108">Класс **мсвм \_ StandaloneV2ElementConformsToProfile** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8549a-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="8549a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="8549a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8549a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8549a-110">Properties</span></span>

<span data-ttu-id="8549a-111">Класс **мсвм \_ StandaloneV2ElementConformsToProfile** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8549a-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8549a-112">**конформантстандард**</span><span class="sxs-lookup"><span data-stu-id="8549a-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8549a-113">Тип данных: **мсвм \_ регистередпрофиле**</span><span class="sxs-lookup"><span data-stu-id="8549a-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="8549a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8549a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8549a-115">Квалификаторы: [ **Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8549a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8549a-116">Зарегистрированный профиль, которому соответствует автономная система.</span><span class="sxs-lookup"><span data-stu-id="8549a-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="8549a-117">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="8549a-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8549a-118">Тип данных: **мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8549a-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8549a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8549a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8549a-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** ("Корневая \\ \\ виртуализация \\ \\ v2")</span><span class="sxs-lookup"><span data-stu-id="8549a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="8549a-121">Автономная система, которая соответствует зарегистрированному профилю.</span><span class="sxs-lookup"><span data-stu-id="8549a-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8549a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8549a-122">Requirements</span></span>



| <span data-ttu-id="8549a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8549a-123">Requirement</span></span> | <span data-ttu-id="8549a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8549a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8549a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8549a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8549a-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8549a-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8549a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8549a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8549a-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8549a-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8549a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8549a-129">Namespace</span></span><br/>                | <span data-ttu-id="8549a-130">Корневое \\ взаимодействие</span><span class="sxs-lookup"><span data-stu-id="8549a-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="8549a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8549a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8549a-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8549a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8549a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8549a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8549a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8549a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8549a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8549a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8549a-136">**Мсвм \_ елементконформстопрофиле**</span><span class="sxs-lookup"><span data-stu-id="8549a-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

