---
description: Представляет параметры для копирования файла с узла на гость.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Класс Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684268"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="8d6a7-103">\_Класс мсвм копифилетогуестсеттингдата</span><span class="sxs-lookup"><span data-stu-id="8d6a7-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="8d6a7-104">Представляет параметры для копирования файла с узла на гость.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="8d6a7-105">Этот класс является производным [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d6a7-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="8d6a7-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d6a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d6a7-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="8d6a7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8d6a7-108">Members</span></span>

<span data-ttu-id="8d6a7-109">Класс **мсвм \_ копифилетогуестсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8d6a7-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8d6a7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d6a7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d6a7-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d6a7-111">Properties</span></span>

<span data-ttu-id="8d6a7-112">Класс **мсвм \_ копифилетогуестсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d6a7-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-116">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8d6a7-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-118">**креатефуллпас**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-121">Указывает, следует ли создавать отсутствующие каталоги в пути к целевому файлу перед копированием файла.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-129">Полный путь к копируемому целевому файлу.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="8d6a7-130">Конечный файл должен быть доступен для гостей и может содержать переменные среды, развернутые гостевыми системами.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="8d6a7-131">Если указанный путь является существующим каталогом в гостевой системе, файл назначения создается в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="8d6a7-132">В этом случае имя файла из **SourcePath** используется в качестве имени целевого файла.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-136">Отображаемое имя для этого экземпляра SettingData.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="8d6a7-137">Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="8d6a7-138">(Примечание. имя не обязательно должно быть уникальным в пределах пространства имен.)</span><span class="sxs-lookup"><span data-stu-id="8d6a7-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-142">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-143">В пределах области создания экземпляра пространства имен InstanceID непрозрачно и уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8d6a7-144">Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма: *OrgID*:*LocalId* , где *OrgID* и *LocalID* разделяются двоеточием (:), и там, где *OrgID* необходимо включать уникальное имя, которое принадлежит бизнес-сущности, которая создает или определяет InstanceId или является зарегистрированным идентификатором, назначенным бизнес-сущности в известном Глобальном центре сертификации.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="8d6a7-145">(Это требование похоже на объект *SchemaName* \_ . Структура *className* имен классов схемы.) Кроме того, чтобы обеспечить уникальность, *OrgID* не должен содержать двоеточия (:).</span><span class="sxs-lookup"><span data-stu-id="8d6a7-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="8d6a7-146">При использовании этого алгоритма первое двоеточие должно появиться в идентификаторе InstanceID между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="8d6a7-147">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="8d6a7-148">Если указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="8d6a7-149">Для экземпляров, определяемых DMTF, необходимо использовать "предпочтительный" алгоритм с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-150">**овервритиксистинг**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-151">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-153">Указывает, нужно ли перезаписывать существующий целевой файл.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="8d6a7-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d6a7-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d6a7-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d6a7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d6a7-157">Полный путь к копируемому исходному файлу.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="8d6a7-158">Этот исходный файл должен быть доступен для узла Hyper-V и может содержать переменные среды, развернутые узлом Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8d6a7-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d6a7-159">Требования</span><span class="sxs-lookup"><span data-stu-id="8d6a7-159">Requirements</span></span>



| <span data-ttu-id="8d6a7-160">Требование</span><span class="sxs-lookup"><span data-stu-id="8d6a7-160">Requirement</span></span> | <span data-ttu-id="8d6a7-161">Значение</span><span class="sxs-lookup"><span data-stu-id="8d6a7-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d6a7-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d6a7-162">Minimum supported client</span></span><br/> | <span data-ttu-id="8d6a7-163">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d6a7-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8d6a7-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d6a7-164">Minimum supported server</span></span><br/> | <span data-ttu-id="8d6a7-165">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d6a7-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d6a7-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8d6a7-166">Namespace</span></span><br/>                | <span data-ttu-id="8d6a7-167">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8d6a7-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8d6a7-168">MOF</span><span class="sxs-lookup"><span data-stu-id="8d6a7-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d6a7-169"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d6a7-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d6a7-170">DLL</span><span class="sxs-lookup"><span data-stu-id="8d6a7-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d6a7-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d6a7-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8d6a7-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d6a7-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d6a7-173">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8d6a7-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="8d6a7-174">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d6a7-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

