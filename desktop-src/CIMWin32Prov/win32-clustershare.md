---
description: Класс Win32 \_ клустершаре представляет общий ресурс в кластере.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Класс Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142307"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="d1d13-103">\_Класс Win32 клустершаре</span><span class="sxs-lookup"><span data-stu-id="d1d13-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="d1d13-104">\[Класс **Win32 \_ клустершаре** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="d1d13-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="d1d13-105">Используйте вместо него [**классы \_ MSFT**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) и [**MSFT \_ смфилешаре**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) .\]</span><span class="sxs-lookup"><span data-stu-id="d1d13-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="d1d13-106">Класс Win32 \_ клустершаре представляет общий ресурс в кластере.</span><span class="sxs-lookup"><span data-stu-id="d1d13-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="d1d13-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d1d13-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d13-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1d13-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
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
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="d1d13-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d1d13-109">Members</span></span>

<span data-ttu-id="d1d13-110">Класс **Win32 \_ клустершаре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1d13-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="d1d13-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d1d13-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1d13-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1d13-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1d13-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d1d13-113">Methods</span></span>

<span data-ttu-id="d1d13-114">Класс **Win32 \_ клустершаре** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d1d13-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="d1d13-115">Метод</span><span class="sxs-lookup"><span data-stu-id="d1d13-115">Method</span></span>                                                    | <span data-ttu-id="d1d13-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d1d13-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="d1d13-117">**Создания**</span><span class="sxs-lookup"><span data-stu-id="d1d13-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="d1d13-118">Создает новый экземпляр **Win32 \_ клустершаре** .</span><span class="sxs-lookup"><span data-stu-id="d1d13-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="d1d13-119">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="d1d13-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="d1d13-120">Удаляет экземпляр **Win32 \_ клустершаре** .</span><span class="sxs-lookup"><span data-stu-id="d1d13-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="d1d13-121">**жетакцессмаск**</span><span class="sxs-lookup"><span data-stu-id="d1d13-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="d1d13-122">Возвращает точечный рисунок с правами доступа к общей папке.</span><span class="sxs-lookup"><span data-stu-id="d1d13-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="d1d13-123">**сетшареинфо**</span><span class="sxs-lookup"><span data-stu-id="d1d13-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="d1d13-124">Задает параметры общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="d1d13-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="d1d13-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1d13-125">Properties</span></span>

<span data-ttu-id="d1d13-126">Класс **Win32 \_ клустершаре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1d13-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1d13-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="d1d13-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d13-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-130">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1d13-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-131">Это свойство устарело и больше не используется.</span><span class="sxs-lookup"><span data-stu-id="d1d13-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="d1d13-132">Вместо этого используйте метод [**Win32 \_ Share. жетакцессмаск**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d13-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="d1d13-133">Для свойства **AccessMask** в WMI устанавливается значение **null** .</span><span class="sxs-lookup"><span data-stu-id="d1d13-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="d1d13-134">Дополнительные сведения о настройке доступа при создании общей папки см. в описании метода [**CREATE**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d13-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="d1d13-135">Это свойство наследуется [**от \_ общего ресурса Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-136">**алловмаксимум**</span><span class="sxs-lookup"><span data-stu-id="d1d13-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1d13-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Общая \_ информация \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ использует")</span><span class="sxs-lookup"><span data-stu-id="d1d13-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-140">Количество одновременных пользователей для этого ресурса ограничено.</span><span class="sxs-lookup"><span data-stu-id="d1d13-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="d1d13-141">При **значении true** значение в свойстве **MaximumAllowed** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d1d13-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="d1d13-142">Это свойство наследуется [**от \_ общего ресурса Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-143">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d1d13-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1d13-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-146">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1d13-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-147">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d13-147">A short textual description of the object.</span></span>

<span data-ttu-id="d1d13-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-149">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1d13-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1d13-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-152">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d1d13-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-153">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d13-153">A textual description of the object.</span></span>

<span data-ttu-id="d1d13-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1d13-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-156">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1d13-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-158">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d1d13-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-159">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="d1d13-159">Indicates when the object was installed.</span></span> <span data-ttu-id="d1d13-160">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="d1d13-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1d13-161">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="d1d13-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d13-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-165">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Общая \_ информация \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ использует")</span><span class="sxs-lookup"><span data-stu-id="d1d13-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-166">Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.</span><span class="sxs-lookup"><span data-stu-id="d1d13-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="d1d13-167">Значение допустимо только в том случае, если свойство **алловмаксимум** имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="d1d13-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="d1d13-168">Это свойство наследуется [**от \_ общего ресурса Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-169">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1d13-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1d13-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-172">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Share \_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="d1d13-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-173">Псевдоним, заданный для пути, настроенного в качестве общего ресурса в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="d1d13-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="d1d13-174">Windows 2008 пример: " \\ Server01 \\ Public" — Windows Server 2008 требует, чтобы в имени был размещен UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="d1d13-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="d1d13-175">Это свойство наследуется [**от \_ общего ресурса Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-176">**Путь**</span><span class="sxs-lookup"><span data-stu-id="d1d13-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1d13-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-179">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Общая \_ информация \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ путь")</span><span class="sxs-lookup"><span data-stu-id="d1d13-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-180">Локальный путь к общей папке Windows.</span><span class="sxs-lookup"><span data-stu-id="d1d13-180">Local path of the Windows share.</span></span>

<span data-ttu-id="d1d13-181">Пример: "C: \\ Program Files"</span><span class="sxs-lookup"><span data-stu-id="d1d13-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="d1d13-182">Это свойство наследуется [**от \_ общего ресурса Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="d1d13-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1d13-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-186">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя_сервера"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Share \_ \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName")</span><span class="sxs-lookup"><span data-stu-id="d1d13-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-187">Сервер кластера, на котором размещена общая папка.</span><span class="sxs-lookup"><span data-stu-id="d1d13-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="d1d13-188">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d1d13-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1d13-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-191">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d1d13-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-192">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d13-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1d13-193">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="d1d13-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1d13-194">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="d1d13-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1d13-195">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="d1d13-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1d13-196">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="d1d13-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1d13-197">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="d1d13-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1d13-198">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d1d13-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1d13-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1d13-200">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d1d13-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1d13-201">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d1d13-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1d13-202">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d1d13-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1d13-203">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d1d13-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1d13-204">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d1d13-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1d13-205">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d1d13-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1d13-206">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d1d13-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1d13-207">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d1d13-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1d13-208">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d1d13-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1d13-209">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d1d13-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1d13-210">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d1d13-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1d13-211">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d1d13-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1d13-212">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d1d13-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1d13-213">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d1d13-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d13-214">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d13-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1d13-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d13-216">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management structures \| [**Share \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Type")</span><span class="sxs-lookup"><span data-stu-id="d1d13-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="d1d13-217">Тип ресурса, к которому предоставляется общий доступ.</span><span class="sxs-lookup"><span data-stu-id="d1d13-217">Type of resource being shared.</span></span> <span data-ttu-id="d1d13-218">К типам относятся: дисковые накопители, очереди печати, межпроцессное взаимодействие (IPC) и общие устройства.</span><span class="sxs-lookup"><span data-stu-id="d1d13-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="d1d13-219">Это свойство наследуется [**от \_ общего ресурса Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="d1d13-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="d1d13-220">**Дисковый накопитель** (0)</span><span class="sxs-lookup"><span data-stu-id="d1d13-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="d1d13-221">**Очередь печати** (1)</span><span class="sxs-lookup"><span data-stu-id="d1d13-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="d1d13-222">**Устройство** (2)</span><span class="sxs-lookup"><span data-stu-id="d1d13-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="d1d13-223">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="d1d13-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="d1d13-224">**Администратор дискового накопителя** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="d1d13-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="d1d13-225">**Администратор очереди печати** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="d1d13-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="d1d13-226">**Администратор устройства** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="d1d13-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="d1d13-227">**Администратор IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="d1d13-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="d1d13-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d1d13-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d1d13-229">Требования</span><span class="sxs-lookup"><span data-stu-id="d1d13-229">Requirements</span></span>



| <span data-ttu-id="d1d13-230">Требование</span><span class="sxs-lookup"><span data-stu-id="d1d13-230">Requirement</span></span> | <span data-ttu-id="d1d13-231">Значение</span><span class="sxs-lookup"><span data-stu-id="d1d13-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d13-232">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1d13-232">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d13-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1d13-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="d1d13-234">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1d13-234">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d13-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1d13-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d1d13-236">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1d13-236">Namespace</span></span><br/>                | <span data-ttu-id="d1d13-237">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1d13-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1d13-238">MOF</span><span class="sxs-lookup"><span data-stu-id="d1d13-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1d13-239"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1d13-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1d13-240">DLL</span><span class="sxs-lookup"><span data-stu-id="d1d13-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1d13-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1d13-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d13-242">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1d13-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d13-243">**\_Общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="d1d13-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

