---
description: '\_Класс подключения CIM представляет связь между файловой системой и каталогом, к которому она присоединена.'
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: Класс CIM_Mount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141896"
---
# <a name="cim_mount-class"></a><span data-ttu-id="ea8f1-103">\_Класс подключения CIM</span><span class="sxs-lookup"><span data-stu-id="ea8f1-103">CIM\_Mount class</span></span>

<span data-ttu-id="ea8f1-104">Класс **\_ подключения CIM** представляет связь между файловой системой и каталогом, к которому она присоединена.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="ea8f1-105">Семантика этой связи требует, чтобы подключенный каталог хранился в файловой системе (через сопоставление хранилища файлов), который отличается от файловой системы, на которую ссылается зависимый файл.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="ea8f1-106">Каталог, содержащий файловую систему, может быть локальным или удаленным.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="ea8f1-107">Например, локальная файловая система на компьютере Solaris может подключить каталог из файловой системы, доступ к которой осуществляется через дисковод CDROM компьютера (то есть в другой локальной файловой системе).</span><span class="sxs-lookup"><span data-stu-id="ea8f1-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="ea8f1-108">С другой стороны, в удаленном случае каталог сначала экспортируется файловой системой, которая размещается в другой компьютерной системе, например, в качестве файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="ea8f1-109">Для различения двух подключений необходимо всегда определять ассоциацию [**\_ экспорта CIM**](cim-export.md) для каталогов с удаленным доступом и удаленных подключений.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea8f1-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ea8f1-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ea8f1-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ea8f1-112">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ea8f1-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8f1-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea8f1-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ea8f1-115">Члены</span><span class="sxs-lookup"><span data-stu-id="ea8f1-115">Members</span></span>

<span data-ttu-id="ea8f1-116">Класс **\_ подключения CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ea8f1-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="ea8f1-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="ea8f1-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea8f1-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="ea8f1-118">Properties</span></span>

<span data-ttu-id="ea8f1-119">Класс **\_ подключения CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea8f1-120">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="ea8f1-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8f1-121">Тип данных: **\_ Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="ea8f1-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="ea8f1-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ea8f1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea8f1-123">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ea8f1-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ea8f1-124">[**\_ Каталог CIM**](cim-directory.md) , описывающий подключенный каталог.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="ea8f1-125">**Него**</span><span class="sxs-lookup"><span data-stu-id="ea8f1-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8f1-126">Тип данных: **CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="ea8f1-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="ea8f1-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ea8f1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea8f1-128">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="ea8f1-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ea8f1-129">[**CIM \_ NFS**](cim-nfs.md) , описывающий файловую систему, к которой подключен каталог.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea8f1-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea8f1-130">Remarks</span></span>

<span data-ttu-id="ea8f1-131">**Модель CIM \_ Подключение** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ea8f1-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ea8f1-132">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-132">WMI does not implement this class.</span></span>

<span data-ttu-id="ea8f1-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ea8f1-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ea8f1-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8f1-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ea8f1-135">Requirements</span></span>



| <span data-ttu-id="ea8f1-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ea8f1-136">Requirement</span></span> | <span data-ttu-id="ea8f1-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ea8f1-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8f1-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea8f1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8f1-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea8f1-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea8f1-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea8f1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8f1-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea8f1-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea8f1-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ea8f1-142">Namespace</span></span><br/>                | <span data-ttu-id="ea8f1-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ea8f1-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea8f1-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ea8f1-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea8f1-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea8f1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8f1-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea8f1-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f1-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8f1-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea8f1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8f1-149">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="ea8f1-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

