---
description: '&Win32 \_ пажефилесеттинг \# 8194; Класс WMI представляет параметры файла подкачки.'
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Класс Win32_PageFileSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656010"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="98877-103">\_Класс Win32 пажефилесеттинг</span><span class="sxs-lookup"><span data-stu-id="98877-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="98877-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ пажефилесеттинг для Win32** представляет параметры файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="98877-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="98877-105">Сведения, содержащиеся в объектах, созданных из этого класса, указывают параметры файла подкачки, используемые при создании файла при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="98877-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="98877-106">Свойства в этом классе можно изменить и отложить до запуска.</span><span class="sxs-lookup"><span data-stu-id="98877-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="98877-107">Эти параметры отличаются от состояния файла подкачки во время выполнения, выраженного в связанном классе [**Win32 \_ пажефилеусаже**](win32-pagefileusage.md).</span><span class="sxs-lookup"><span data-stu-id="98877-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="98877-108">Чтобы создать экземпляр этого класса, включите привилегию **секреатепажефилепривилеже** .</span><span class="sxs-lookup"><span data-stu-id="98877-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="98877-109">Дополнительные сведения см. в статьях [**константы прав**](../wmisdk/privilege-constants.md) и [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="98877-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="98877-110">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="98877-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="98877-111">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="98877-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98877-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98877-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="98877-113">Члены</span><span class="sxs-lookup"><span data-stu-id="98877-113">Members</span></span>

<span data-ttu-id="98877-114">Класс **Win32 \_ пажефилесеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="98877-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="98877-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="98877-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98877-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="98877-116">Properties</span></span>

<span data-ttu-id="98877-117">Класс **Win32 \_ пажефилесеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="98877-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98877-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="98877-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98877-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98877-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98877-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98877-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98877-121">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="98877-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="98877-122">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="98877-122">Short textual description of the current object.</span></span>

<span data-ttu-id="98877-123">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="98877-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="98877-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98877-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98877-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98877-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98877-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98877-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98877-127">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="98877-127">Textual description of the current object.</span></span>

<span data-ttu-id="98877-128">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="98877-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="98877-129">**инитиалсизе**</span><span class="sxs-lookup"><span data-stu-id="98877-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98877-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98877-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98877-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="98877-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98877-132">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Управление \\ \\ \\ \\ памятью диспетчер сеансов \| пагингфилес"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="98877-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="98877-133">Начальный размер файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="98877-133">Initial size of the page file.</span></span>

<span data-ttu-id="98877-134">Пример: 139</span><span class="sxs-lookup"><span data-stu-id="98877-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="98877-135">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="98877-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98877-136">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98877-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98877-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="98877-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98877-138">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Управление \\ \\ \\ \\ памятью диспетчер сеансов \| пагингфилес"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="98877-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="98877-139">Максимальный размер файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="98877-139">Maximum size of the page file.</span></span>

<span data-ttu-id="98877-140">Пример: 178</span><span class="sxs-lookup"><span data-stu-id="98877-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="98877-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="98877-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98877-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98877-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98877-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="98877-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98877-144">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="98877-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="98877-145">Путь и имя файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="98877-145">Path and file name of the page file.</span></span>

<span data-ttu-id="98877-146">Пример: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="98877-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="98877-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="98877-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98877-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98877-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98877-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98877-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98877-150">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="98877-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="98877-151">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="98877-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="98877-152">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="98877-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98877-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98877-153">Remarks</span></span>

<span data-ttu-id="98877-154">Класс **Win32 \_ пажефилесеттинг** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="98877-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98877-155">Требования</span><span class="sxs-lookup"><span data-stu-id="98877-155">Requirements</span></span>



| <span data-ttu-id="98877-156">Требование</span><span class="sxs-lookup"><span data-stu-id="98877-156">Requirement</span></span> | <span data-ttu-id="98877-157">Значение</span><span class="sxs-lookup"><span data-stu-id="98877-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98877-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98877-158">Minimum supported client</span></span><br/> | <span data-ttu-id="98877-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98877-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98877-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98877-160">Minimum supported server</span></span><br/> | <span data-ttu-id="98877-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98877-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98877-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="98877-162">Namespace</span></span><br/>                | <span data-ttu-id="98877-163">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="98877-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98877-164">MOF</span><span class="sxs-lookup"><span data-stu-id="98877-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98877-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98877-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98877-166">DLL</span><span class="sxs-lookup"><span data-stu-id="98877-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98877-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98877-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98877-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98877-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98877-169">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="98877-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="98877-170">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="98877-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
