---
title: Класс MSAD_NamingContext
description: Представляет определенный контекст именования (NC) на контроллере домена.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- Класс MSAD_NamingContext Active Directory
- Active Directory класса MSAD_NamingContext, описание
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802339"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="c5601-105">\_Класс МСАД намингконтекст</span><span class="sxs-lookup"><span data-stu-id="c5601-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="c5601-106">Представляет определенный контекст именования (NC) на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="c5601-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5601-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5601-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="c5601-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c5601-108">Members</span></span>

<span data-ttu-id="c5601-109">Класс **МСАД \_ намингконтекст** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c5601-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="c5601-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5601-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5601-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5601-111">Properties</span></span>

<span data-ttu-id="c5601-112">Класс **МСАД \_ намингконтекст** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c5601-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5601-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="c5601-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5601-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5601-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c5601-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5601-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5601-116">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5601-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5601-117">Возвращает путь X. 500 NC.</span><span class="sxs-lookup"><span data-stu-id="c5601-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="c5601-118">**исфуллреплика**</span><span class="sxs-lookup"><span data-stu-id="c5601-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5601-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c5601-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5601-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5601-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5601-121">Возвращает значение, указывающее, доступен ли NC для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c5601-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="c5601-122">**Значение true** , если NC доступен для чтения и записи; **Значение false** , если NC доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5601-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5601-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c5601-123">Requirements</span></span>



| <span data-ttu-id="c5601-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c5601-124">Requirement</span></span> | <span data-ttu-id="c5601-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c5601-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5601-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5601-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c5601-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c5601-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c5601-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5601-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c5601-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5601-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5601-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c5601-130">Namespace</span></span><br/>                | <span data-ttu-id="c5601-131">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="c5601-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="c5601-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c5601-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5601-133"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5601-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5601-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c5601-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5601-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5601-135"><dt>Replprov.dll</dt></span></span> </dl> |



 

