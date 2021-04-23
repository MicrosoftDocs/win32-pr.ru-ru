---
description: Класс CIM \_ филеспеЦификатион представляет файл, который либо включен, либо выключен в системе.
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: Класс CIM_FileSpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650448"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="9948d-103">\_Класс CIM филеспеЦификатион</span><span class="sxs-lookup"><span data-stu-id="9948d-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="9948d-104">Класс **CIM \_ филеспеЦификатион** представляет файл, который либо включен, либо выключен в системе.</span><span class="sxs-lookup"><span data-stu-id="9948d-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="9948d-105">Файл находится в каталоге, определенном Ассоциацией [**CIM \_ директориспеЦификатионфиле**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="9948d-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="9948d-106">Метод [**Invoke**](invoke-method-in-class-cim-filespecification.md) использует сведения для проверки существования файла.</span><span class="sxs-lookup"><span data-stu-id="9948d-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="9948d-107">Обратите внимание, что свойства со значением **null** не проверяются.</span><span class="sxs-lookup"><span data-stu-id="9948d-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9948d-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9948d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9948d-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9948d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9948d-110">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9948d-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9948d-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9948d-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9948d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9948d-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="9948d-113">Члены</span><span class="sxs-lookup"><span data-stu-id="9948d-113">Members</span></span>

<span data-ttu-id="9948d-114">Класс **CIM \_ филеспеЦификатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9948d-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="9948d-115">Методы</span><span class="sxs-lookup"><span data-stu-id="9948d-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="9948d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="9948d-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9948d-117">Методы</span><span class="sxs-lookup"><span data-stu-id="9948d-117">Methods</span></span>

<span data-ttu-id="9948d-118">Класс **CIM \_ филеспеЦификатион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9948d-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="9948d-119">Метод</span><span class="sxs-lookup"><span data-stu-id="9948d-119">Method</span></span>                                                         | <span data-ttu-id="9948d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9948d-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="9948d-121">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="9948d-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="9948d-122">Оценивает определенную проверку.</span><span class="sxs-lookup"><span data-stu-id="9948d-122">Evaluates a particular check.</span></span> <span data-ttu-id="9948d-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9948d-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9948d-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="9948d-124">Properties</span></span>

<span data-ttu-id="9948d-125">Класс **CIM \_ филеспеЦификатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9948d-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9948d-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9948d-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9948d-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-130">Краткое текстовое описание субъекта.</span><span class="sxs-lookup"><span data-stu-id="9948d-130">A short textual description of the subject.</span></span>

<span data-ttu-id="9948d-131">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="9948d-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-135">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9948d-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-136">Идентификатор, используемый в сочетании с другими ключами для уникальной идентификации проверки.</span><span class="sxs-lookup"><span data-stu-id="9948d-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="9948d-137">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-138">**чеккмоде**</span><span class="sxs-lookup"><span data-stu-id="9948d-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9948d-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9948d-141">Если **значение равно true**, то условие должно существовать в среде.</span><span class="sxs-lookup"><span data-stu-id="9948d-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="9948d-142">Например, предполагается, что файл находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="9948d-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="9948d-143">Если **значение равно false**, условие не должно существовать.</span><span class="sxs-lookup"><span data-stu-id="9948d-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="9948d-144">Например, файл не находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9948d-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="9948d-145">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-146">**Вычислен**</span><span class="sxs-lookup"><span data-stu-id="9948d-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9948d-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-149">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сигнатура по DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="9948d-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="9948d-150">Значение вычисляется как 16-разрядная сумма первых 32 байт файла.</span><span class="sxs-lookup"><span data-stu-id="9948d-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9948d-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="9948d-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9948d-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-154">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сигнатура по DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="9948d-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9948d-155">Значение CRC, вычисленное с использованием середины 512 КБ.</span><span class="sxs-lookup"><span data-stu-id="9948d-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="9948d-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="9948d-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9948d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-159">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сигнатура по DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="9948d-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="9948d-160">Значение CRC для середины 512 КБ файла, остаток от деления 3.</span><span class="sxs-lookup"><span data-stu-id="9948d-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="9948d-161">**креатетиместамп**</span><span class="sxs-lookup"><span data-stu-id="9948d-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-162">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9948d-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-164">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9948d-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-165">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="9948d-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="9948d-166">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9948d-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9948d-169">Описание объектов.</span><span class="sxs-lookup"><span data-stu-id="9948d-169">A description of the objects.</span></span>

<span data-ttu-id="9948d-170">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-171">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="9948d-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-172">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9948d-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-174">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="9948d-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9948d-175">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="9948d-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="9948d-176">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9948d-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="9948d-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-180">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span><span class="sxs-lookup"><span data-stu-id="9948d-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-181">Алгоритм вычисления 128-разрядной контрольной суммы для любого файла или объекта.</span><span class="sxs-lookup"><span data-stu-id="9948d-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="9948d-182">Вероятность того, что два разных файла, создающие одну и ту же контрольную сумму MD5, очень мала (около 1 в 2 ^ 64), а контрольная сумма MD5 файла может использоваться для создания надежного идентификатора содержимого, который, скорее всего, будет уникальным образом идентифицировать файл.</span><span class="sxs-lookup"><span data-stu-id="9948d-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="9948d-183">То же самое будет наблюдаться и в обратной ситуации.</span><span class="sxs-lookup"><span data-stu-id="9948d-183">The reverse is also true.</span></span> <span data-ttu-id="9948d-184">Если два файла имеют одинаковую контрольную сумму MD5, вполне вероятно, что файлы идентичны.</span><span class="sxs-lookup"><span data-stu-id="9948d-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="9948d-185">Для целей спецификации MOF свойства MD5 алгоритм MD5 всегда создает строку из 32 символов.</span><span class="sxs-lookup"><span data-stu-id="9948d-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="9948d-186">Например, строка "абкдефгхижклмнопкрстуввксиз" создает строку "c3fcd3d76192e4007dfb496cca67e13b".</span><span class="sxs-lookup"><span data-stu-id="9948d-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="9948d-187">Дополнительные сведения о реализации алгоритма MD5 см. в [документе RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span><span class="sxs-lookup"><span data-stu-id="9948d-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-188">**Name**</span><span class="sxs-lookup"><span data-stu-id="9948d-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-191">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="9948d-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-192">Либо имя файла, либо имя файла с префиксом каталога.</span><span class="sxs-lookup"><span data-stu-id="9948d-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="9948d-193">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="9948d-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-196">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9948d-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-197">Это идентификатор этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="9948d-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="9948d-198">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9948d-199">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="9948d-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-200">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9948d-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-202">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9948d-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9948d-203">Состояние программного элемента программного элемента.</span><span class="sxs-lookup"><span data-stu-id="9948d-203">The software element state of a software element.</span></span>

<span data-ttu-id="9948d-204">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9948d-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="9948d-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-206">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="9948d-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9948d-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="9948d-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-208">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="9948d-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9948d-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="9948d-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-210">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="9948d-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9948d-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="9948d-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-212">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="9948d-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9948d-213">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="9948d-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-214">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9948d-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-216">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="9948d-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9948d-217">Целевая операционная система программного элемента.</span><span class="sxs-lookup"><span data-stu-id="9948d-217">Target operating system of the software element.</span></span>

<span data-ttu-id="9948d-218">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9948d-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9948d-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9948d-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9948d-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9948d-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="9948d-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-222">MacOS</span><span class="sxs-lookup"><span data-stu-id="9948d-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9948d-223"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="9948d-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-224">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="9948d-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9948d-225"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="9948d-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9948d-226"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="9948d-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9948d-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="9948d-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9948d-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="9948d-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-229">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="9948d-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9948d-230"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="9948d-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9948d-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9948d-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="9948d-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9948d-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="9948d-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9948d-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="9948d-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9948d-235"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="9948d-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9948d-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="9948d-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-237">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="9948d-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9948d-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="9948d-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9948d-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="9948d-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-240">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="9948d-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9948d-241"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="9948d-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9948d-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9948d-243"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="9948d-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9948d-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9948d-245"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="9948d-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9948d-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9948d-247"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="9948d-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9948d-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9948d-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="9948d-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-250">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="9948d-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9948d-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="9948d-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9948d-252"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="9948d-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9948d-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="9948d-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9948d-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="9948d-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9948d-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="9948d-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9948d-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="9948d-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9948d-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="9948d-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9948d-258"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="9948d-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9948d-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="9948d-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9948d-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="9948d-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9948d-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="9948d-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9948d-262"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="9948d-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-263">Серия</span><span class="sxs-lookup"><span data-stu-id="9948d-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9948d-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="9948d-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-265">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="9948d-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9948d-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="9948d-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-267">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="9948d-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9948d-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="9948d-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9948d-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9948d-270"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="9948d-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9948d-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="9948d-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9948d-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="9948d-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9948d-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="9948d-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9948d-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="9948d-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9948d-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="9948d-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-276">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="9948d-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9948d-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="9948d-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9948d-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="9948d-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9948d-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="9948d-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9948d-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="9948d-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9948d-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9948d-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="9948d-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9948d-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="9948d-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9948d-284"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="9948d-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9948d-285"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="9948d-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9948d-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="9948d-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9948d-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="9948d-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9948d-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="9948d-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9948d-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="9948d-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9948d-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="9948d-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9948d-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="9948d-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9948d-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="9948d-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9948d-293">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="9948d-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9948d-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="9948d-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9948d-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="9948d-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9948d-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="9948d-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9948d-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="9948d-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9948d-298"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="9948d-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9948d-299">**Version**</span><span class="sxs-lookup"><span data-stu-id="9948d-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9948d-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9948d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9948d-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9948d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9948d-302">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="9948d-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9948d-303">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="9948d-303">Version of the operation.</span></span>

<span data-ttu-id="9948d-304">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="9948d-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9948d-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9948d-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9948d-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9948d-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="9948d-307">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9948d-308">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9948d-308">Remarks</span></span>

<span data-ttu-id="9948d-309">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="9948d-309">WMI does not implement this class.</span></span> <span data-ttu-id="9948d-310">Классы, производные от **CIM \_ филеспеЦификатион**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9948d-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9948d-311">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9948d-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9948d-312">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9948d-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9948d-313">Требования</span><span class="sxs-lookup"><span data-stu-id="9948d-313">Requirements</span></span>



| <span data-ttu-id="9948d-314">Требование</span><span class="sxs-lookup"><span data-stu-id="9948d-314">Requirement</span></span> | <span data-ttu-id="9948d-315">Значение</span><span class="sxs-lookup"><span data-stu-id="9948d-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9948d-316">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9948d-316">Minimum supported client</span></span><br/> | <span data-ttu-id="9948d-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9948d-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9948d-318">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9948d-318">Minimum supported server</span></span><br/> | <span data-ttu-id="9948d-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9948d-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9948d-320">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9948d-320">Namespace</span></span><br/>                | <span data-ttu-id="9948d-321">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9948d-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9948d-322">MOF</span><span class="sxs-lookup"><span data-stu-id="9948d-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9948d-323"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9948d-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9948d-324">DLL</span><span class="sxs-lookup"><span data-stu-id="9948d-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9948d-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9948d-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9948d-326">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9948d-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9948d-327">**\_Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="9948d-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

