---
description: '\_Класс общих ресурсов Win32 представляет общий ресурс в компьютерной системе под Windows. Это может быть дисковый накопитель, принтер, межпроцессный обмен данными или другое устройство, доступное для совместного выполнения. Дополнительные сведения о получении классов WMI см. в разделе Получение класса.'
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Класс Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142256"
---
# <a name="win32_share-class"></a><span data-ttu-id="6b0a9-105">\_Класс общего ресурса Win32</span><span class="sxs-lookup"><span data-stu-id="6b0a9-105">Win32\_Share class</span></span>

<span data-ttu-id="6b0a9-106">Класс **\_ общих ресурсов Win32** представляет общий ресурс в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="6b0a9-107">Это может быть дисковый накопитель, принтер, межпроцессный обмен данными или другое устройство, доступное для совместного выполнения.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="6b0a9-108">Дополнительные сведения о получении классов WMI см. в разделе [Получение класса](../wmisdk/retrieving-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="6b0a9-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6b0a9-110">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0a9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b0a9-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="6b0a9-112">Члены</span><span class="sxs-lookup"><span data-stu-id="6b0a9-112">Members</span></span>

<span data-ttu-id="6b0a9-113">Класс **\_ общего ресурса Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6b0a9-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="6b0a9-114">Методы</span><span class="sxs-lookup"><span data-stu-id="6b0a9-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6b0a9-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b0a9-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b0a9-116">Методы</span><span class="sxs-lookup"><span data-stu-id="6b0a9-116">Methods</span></span>

<span data-ttu-id="6b0a9-117">Класс **\_ общего ресурса Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="6b0a9-118">Метод</span><span class="sxs-lookup"><span data-stu-id="6b0a9-118">Method</span></span>                                                             | <span data-ttu-id="6b0a9-119">Описание</span><span class="sxs-lookup"><span data-stu-id="6b0a9-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b0a9-120">**Создания**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="6b0a9-121">Метод класса, инициирующий совместное использование ресурса сервера.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="6b0a9-122">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="6b0a9-123">Метод класса, который удаляет имя общего ресурса из списка общих ресурсов сервера, отключая подключения к общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="6b0a9-124">**жетакцессмаск**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="6b0a9-125">Возвращает права доступа к общей папке, удерживаемой пользователем или группой, от имени которой возвращается экземпляр.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="6b0a9-126">Этот метод следует использовать вместо свойства **AccessMask** , которое всегда имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="6b0a9-127">**сетшареинфо**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="6b0a9-128">Метод класса, который задает параметры общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="6b0a9-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b0a9-129">Properties</span></span>

<span data-ttu-id="6b0a9-130">Класс **\_ общего ресурса Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b0a9-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-134">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-135">Это свойство устарело и больше не используется.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="6b0a9-136">Вместо этого используйте метод [**Win32 \_ Share. жетакцессмаск**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0a9-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="6b0a9-137">Для свойства **AccessMask** в WMI устанавливается значение **null** .</span><span class="sxs-lookup"><span data-stu-id="6b0a9-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="6b0a9-138">Дополнительные сведения о настройке доступа при создании общей папки см. в описании метода [**CREATE**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0a9-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-139">**алловмаксимум**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-142">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Общая \_ информация \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ использует")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-143">Количество одновременных пользователей для этого ресурса ограничено.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="6b0a9-144">При **значении true** значение в свойстве **MaximumAllowed** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-145">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-148">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-149">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-149">A short textual description of the object.</span></span>

<span data-ttu-id="6b0a9-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-151">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-154">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-155">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-155">A textual description of the object.</span></span>

<span data-ttu-id="6b0a9-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-158">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-160">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-161">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-161">Indicates when the object was installed.</span></span> <span data-ttu-id="6b0a9-162">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6b0a9-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-167">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Общая \_ информация \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ использует")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-168">Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="6b0a9-169">Значение допустимо только в том случае, если свойство **алловмаксимум** имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-170">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-173">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Share \_ \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-174">Псевдоним, заданный для пути, настроенного в качестве общего ресурса в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="6b0a9-175">Windows 2008 пример: " \\ Server01 \\ Public" — Windows Server 2008 требует, чтобы в имени был размещен UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-176">**Путь**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-179">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Общая \_ информация \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ путь")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-180">Локальный путь к общей папке Windows.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-180">Local path of the Windows share.</span></span>

<span data-ttu-id="6b0a9-181">Пример: "C: \\ Program Files"</span><span class="sxs-lookup"><span data-stu-id="6b0a9-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="6b0a9-182">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-185">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-186">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="6b0a9-187">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6b0a9-188">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="6b0a9-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6b0a9-189">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6b0a9-190">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="6b0a9-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6b0a9-191">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6b0a9-192">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6b0a9-193">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6b0a9-194">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6b0a9-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6b0a9-195">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6b0a9-196">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b0a9-197">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b0a9-198">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6b0a9-199">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6b0a9-200">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6b0a9-201">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6b0a9-202">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6b0a9-203">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6b0a9-204">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6b0a9-205">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6b0a9-206">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b0a9-207">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b0a9-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b0a9-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b0a9-210">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management structures \| [**Share \_ \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Type")</span><span class="sxs-lookup"><span data-stu-id="6b0a9-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="6b0a9-211">Тип ресурса, к которому предоставляется общий доступ.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-211">Type of resource being shared.</span></span> <span data-ttu-id="6b0a9-212">К типам относятся: дисковые накопители, очереди печати, межпроцессное взаимодействие (IPC) и общие устройства.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="6b0a9-213">**Дисковый накопитель** (0)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="6b0a9-214">**Очередь печати** (1)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="6b0a9-215">**Устройство** (2)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="6b0a9-216">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="6b0a9-217">**Администратор дискового накопителя** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="6b0a9-218">**Администратор очереди печати** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="6b0a9-219">**Администратор устройства** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="6b0a9-220">**Администратор IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="6b0a9-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="6b0a9-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6b0a9-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6b0a9-222">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b0a9-222">Remarks</span></span>

<span data-ttu-id="6b0a9-223">Класс **\_ общего ресурса Win32** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a9-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="6b0a9-224">Метод Create в этом классе является статическим методом.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="6b0a9-225">Методы **Delete**, **жетакцессмаск** и **сетшареинфо** являются методами экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="6b0a9-226">В зависимости от разрешений безопасности, возможно, вам не удастся получить все свойства этого класса.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="6b0a9-227">Например, свойства **алловмаксимум**, **MaximumAllowed**, **path** и **Type** могут возвращать значение null.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="6b0a9-228">В целом, опытные пользователи и администраторы смогут получать все значения свойств.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="6b0a9-229">Примеры</span><span class="sxs-lookup"><span data-stu-id="6b0a9-229">Examples</span></span>

<span data-ttu-id="6b0a9-230">В следующем[примере кода](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) в центре сценариев перечислены все общие папки на компьютере и перечислены все разрешения общего доступа для каждой общей папки.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="6b0a9-231">[Сведения о том, как получить общий доступ к общему \_ ](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) ресурсу PowerShell, см. в этой общей \_ папке Win32 и предоставляет результаты.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="6b0a9-232">В следующем примере PowerShell отображаются общие папки в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="6b0a9-233">Кроме того, если вы хотите отфильтровать более точно, можно использовать следующий фрагмент кода PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6b0a9-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="6b0a9-234">В следующем примере VBScript отображаются общие папки в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="6b0a9-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="6b0a9-235">Требования</span><span class="sxs-lookup"><span data-stu-id="6b0a9-235">Requirements</span></span>



| <span data-ttu-id="6b0a9-236">Требование</span><span class="sxs-lookup"><span data-stu-id="6b0a9-236">Requirement</span></span> | <span data-ttu-id="6b0a9-237">Значение</span><span class="sxs-lookup"><span data-stu-id="6b0a9-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0a9-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b0a9-238">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0a9-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b0a9-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b0a9-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b0a9-240">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0a9-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b0a9-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b0a9-242">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b0a9-242">Namespace</span></span><br/>                | <span data-ttu-id="6b0a9-243">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b0a9-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b0a9-244">MOF</span><span class="sxs-lookup"><span data-stu-id="6b0a9-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b0a9-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b0a9-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b0a9-246">DLL</span><span class="sxs-lookup"><span data-stu-id="6b0a9-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b0a9-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b0a9-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0a9-248">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b0a9-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0a9-249">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="6b0a9-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="6b0a9-250">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="6b0a9-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6b0a9-251">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="6b0a9-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
