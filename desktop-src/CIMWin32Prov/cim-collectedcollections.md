---
description: Класс CIM \_ коллектедколлектионс является ассоциацией статистической обработки, представляющей коллекцию управляемых системных элементов (MSE), содержащихся в коллекции мсес.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: Класс CIM_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990640"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="84462-103">\_Класс CIM коллектедколлектионс</span><span class="sxs-lookup"><span data-stu-id="84462-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="84462-104">Класс **CIM \_ коллектедколлектионс** является ассоциацией статистической обработки, представляющей коллекцию управляемых СИСТЕМНЫХ элементов (MSE), содержащихся в коллекции мсес.</span><span class="sxs-lookup"><span data-stu-id="84462-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84462-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="84462-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="84462-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="84462-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="84462-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="84462-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="84462-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="84462-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84462-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84462-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="84462-110">Члены</span><span class="sxs-lookup"><span data-stu-id="84462-110">Members</span></span>

<span data-ttu-id="84462-111">Класс **CIM \_ коллектедколлектионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84462-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="84462-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="84462-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84462-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="84462-113">Properties</span></span>

<span data-ttu-id="84462-114">Класс **CIM \_ коллектедколлектионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84462-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84462-115">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="84462-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84462-116">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="84462-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="84462-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84462-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84462-118">Ссылка на родительский элемент "более высокий уровень" или в агрегате.</span><span class="sxs-lookup"><span data-stu-id="84462-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="84462-119">**коллектионинколлектион**</span><span class="sxs-lookup"><span data-stu-id="84462-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84462-120">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="84462-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="84462-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84462-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84462-122">Ссылка на собранную **коллекцию**.</span><span class="sxs-lookup"><span data-stu-id="84462-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84462-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84462-123">Remarks</span></span>

<span data-ttu-id="84462-124">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="84462-124">WMI does not implement this class.</span></span>

<span data-ttu-id="84462-125">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="84462-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="84462-126">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="84462-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="84462-127">Требования</span><span class="sxs-lookup"><span data-stu-id="84462-127">Requirements</span></span>



| <span data-ttu-id="84462-128">Требование</span><span class="sxs-lookup"><span data-stu-id="84462-128">Requirement</span></span> | <span data-ttu-id="84462-129">Значение</span><span class="sxs-lookup"><span data-stu-id="84462-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84462-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84462-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84462-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84462-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84462-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84462-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84462-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84462-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84462-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84462-134">Namespace</span></span><br/>                | <span data-ttu-id="84462-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84462-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84462-136">MOF</span><span class="sxs-lookup"><span data-stu-id="84462-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84462-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84462-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84462-138">DLL</span><span class="sxs-lookup"><span data-stu-id="84462-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84462-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84462-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




