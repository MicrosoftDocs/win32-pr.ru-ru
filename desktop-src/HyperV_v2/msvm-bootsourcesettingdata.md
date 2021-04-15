---
description: Представляет параметры для задания источника загрузки виртуальной машины.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Класс Msvm_BootSourceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682936"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="11416-103">\_Класс мсвм бутсаурцесеттингдата</span><span class="sxs-lookup"><span data-stu-id="11416-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="11416-104">Представляет параметры для задания источника загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="11416-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="11416-105">Этот класс является производным [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11416-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="11416-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="11416-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11416-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11416-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="11416-108">Члены</span><span class="sxs-lookup"><span data-stu-id="11416-108">Members</span></span>

<span data-ttu-id="11416-109">Класс **мсвм \_ бутсаурцесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11416-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="11416-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="11416-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11416-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="11416-111">Properties</span></span>

<span data-ttu-id="11416-112">Класс **мсвм \_ бутсаурцесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11416-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11416-113">**бутсаурцедескриптион**</span><span class="sxs-lookup"><span data-stu-id="11416-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11416-116">Описание источника загрузки, предоставленное встроенным по.</span><span class="sxs-lookup"><span data-stu-id="11416-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="11416-117">**бутсаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="11416-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11416-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11416-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11416-120">Значение перечисления, указывающее тип источника загрузки.</span><span class="sxs-lookup"><span data-stu-id="11416-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="11416-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="11416-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11416-122">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="11416-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="11416-123">**Диск** (1)</span><span class="sxs-lookup"><span data-stu-id="11416-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="11416-124">**Сеть** (2)</span><span class="sxs-lookup"><span data-stu-id="11416-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="11416-125">**Файл** (3)</span><span class="sxs-lookup"><span data-stu-id="11416-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11416-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="11416-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11416-129">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="11416-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="11416-130">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="11416-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="11416-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="11416-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11416-134">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="11416-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="11416-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="11416-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11416-138">Отображаемое имя для этого экземпляра SettingData.</span><span class="sxs-lookup"><span data-stu-id="11416-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="11416-139">Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="11416-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="11416-140">(Примечание. имя не обязательно должно быть уникальным в пределах пространства имен.)</span><span class="sxs-lookup"><span data-stu-id="11416-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="11416-141">**фирмваредевицепас**</span><span class="sxs-lookup"><span data-stu-id="11416-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11416-144">Собственный путь, который используется встроенным по для описания устройства.</span><span class="sxs-lookup"><span data-stu-id="11416-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="11416-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11416-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11416-148">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="11416-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="11416-149">В пределах области создания экземпляра пространства имен InstanceID непрозрачно и уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="11416-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="11416-150">Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма: *OrgID*:*LocalId* , где *OrgID* и *LocalID* разделяются двоеточием (:), и там, где *OrgID* необходимо включать уникальное имя, которое принадлежит бизнес-сущности, которая создает или определяет InstanceId или является зарегистрированным идентификатором, назначенным бизнес-сущности в известном Глобальном центре сертификации.</span><span class="sxs-lookup"><span data-stu-id="11416-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="11416-151">(Это требование похоже на объект *SchemaName* \_ . Структура *className* имен классов схемы.) Кроме того, чтобы обеспечить уникальность, *OrgID* не должен содержать двоеточия (:).</span><span class="sxs-lookup"><span data-stu-id="11416-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="11416-152">При использовании этого алгоритма первое двоеточие должно появиться в идентификаторе InstanceID между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="11416-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="11416-153">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов.</span><span class="sxs-lookup"><span data-stu-id="11416-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="11416-154">Если указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11416-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="11416-155">Для экземпляров, определяемых DMTF, необходимо использовать "предпочтительный" алгоритм с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="11416-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="11416-156">**оптионалдата**</span><span class="sxs-lookup"><span data-stu-id="11416-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-157">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="11416-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="11416-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11416-159">Квалификаторы: **октетстринг**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Индексировано")</span><span class="sxs-lookup"><span data-stu-id="11416-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="11416-160">Необязательные данные, предоставляемые встроенным по.</span><span class="sxs-lookup"><span data-stu-id="11416-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="11416-161">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="11416-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="11416-162">**осерлокатион**</span><span class="sxs-lookup"><span data-stu-id="11416-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11416-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11416-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11416-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11416-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11416-165">Другие сведения о расположении (если таковые имеются), используемые встроенным по для дальнейшей уникальной идентификации источника загрузки.</span><span class="sxs-lookup"><span data-stu-id="11416-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11416-166">Требования</span><span class="sxs-lookup"><span data-stu-id="11416-166">Requirements</span></span>



| <span data-ttu-id="11416-167">Требование</span><span class="sxs-lookup"><span data-stu-id="11416-167">Requirement</span></span> | <span data-ttu-id="11416-168">Значение</span><span class="sxs-lookup"><span data-stu-id="11416-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11416-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11416-169">Minimum supported client</span></span><br/> | <span data-ttu-id="11416-170">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11416-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="11416-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11416-171">Minimum supported server</span></span><br/> | <span data-ttu-id="11416-172">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="11416-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11416-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11416-173">Namespace</span></span><br/>                | <span data-ttu-id="11416-174">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="11416-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="11416-175">MOF</span><span class="sxs-lookup"><span data-stu-id="11416-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11416-176"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11416-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11416-177">DLL</span><span class="sxs-lookup"><span data-stu-id="11416-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11416-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11416-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11416-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11416-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11416-180">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="11416-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="11416-181">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11416-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

