---
description: Используется для связывания экземпляра CIM \_ регистередпрофиле с экземпляром CIM \_ регистередпрофиле другого профиля, который ссылается на зависимый профиль в качестве связанного профиля.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Класс CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647573"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="c912e-103">\_Класс CIM референцедпрофиле</span><span class="sxs-lookup"><span data-stu-id="c912e-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="c912e-104">Используется для связывания экземпляра [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) с экземпляром **CIM \_ регистередпрофиле** другого профиля, который ссылается на зависимый профиль в качестве связанного профиля.</span><span class="sxs-lookup"><span data-stu-id="c912e-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c912e-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c912e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c912e-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c912e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c912e-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c912e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c912e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c912e-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c912e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c912e-109">Members</span></span>

<span data-ttu-id="c912e-110">Класс **CIM \_ референцедпрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c912e-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="c912e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c912e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c912e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c912e-112">Properties</span></span>

<span data-ttu-id="c912e-113">Класс **CIM \_ референцедпрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c912e-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c912e-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c912e-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c912e-115">Тип данных: **[ **CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c912e-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="c912e-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c912e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c912e-117">Указывает экземпляр [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) , на который ссылается **зависимый** профиль.</span><span class="sxs-lookup"><span data-stu-id="c912e-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="c912e-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="c912e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c912e-119">Тип данных: **[ **CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c912e-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="c912e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c912e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c912e-121">Указывает экземпляр [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) , который ссылается на другие профили.</span><span class="sxs-lookup"><span data-stu-id="c912e-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c912e-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c912e-122">Remarks</span></span>

<span data-ttu-id="c912e-123">Использование свойств **Dependent** и **Antecedent** в ассоциации **CIM \_ референцедпрофиле** определено таким образом, что к профилю, на который указывает ссылка, относится предшествующая задача, а профиль, ссылающийся на ссылку, является зависимым.</span><span class="sxs-lookup"><span data-stu-id="c912e-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="c912e-124">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c912e-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c912e-125">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c912e-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c912e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c912e-126">Requirements</span></span>



| <span data-ttu-id="c912e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c912e-127">Requirement</span></span> | <span data-ttu-id="c912e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c912e-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c912e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c912e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c912e-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c912e-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="c912e-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c912e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c912e-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c912e-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="c912e-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c912e-133">Namespace</span></span><br/>                | <span data-ttu-id="c912e-134">Корневое \\ взаимодействие</span><span class="sxs-lookup"><span data-stu-id="c912e-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="c912e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c912e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c912e-136"><dt>Interop. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c912e-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c912e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c912e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c912e-138">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="c912e-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

