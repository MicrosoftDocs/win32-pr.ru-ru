---
description: Класс CIM \_ суппортакцесс определяет, как получить помощь для продукта.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: Класс CIM_SupportAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141584"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="01c0b-103">\_Класс CIM суппортакцесс</span><span class="sxs-lookup"><span data-stu-id="01c0b-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="01c0b-104">Класс **CIM \_ суппортакцесс** определяет, как получить помощь для продукта.</span><span class="sxs-lookup"><span data-stu-id="01c0b-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01c0b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="01c0b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01c0b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01c0b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01c0b-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="01c0b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="01c0b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="01c0b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c0b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01c0b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="01c0b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="01c0b-110">Members</span></span>

<span data-ttu-id="01c0b-111">Класс **CIM \_ суппортакцесс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="01c0b-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="01c0b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="01c0b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01c0b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="01c0b-113">Properties</span></span>

<span data-ttu-id="01c0b-114">Класс **CIM \_ суппортакцесс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="01c0b-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01c0b-115">**коммуникатионинфо**</span><span class="sxs-lookup"><span data-stu-id="01c0b-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="01c0b-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01c0b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| FRU \| 002,11 "," MIF. DMTF \| FRU \| 002,12 ")</span><span class="sxs-lookup"><span data-stu-id="01c0b-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-119">Сведения о режиме связи.</span><span class="sxs-lookup"><span data-stu-id="01c0b-119">Details of the communication mode.</span></span> <span data-ttu-id="01c0b-120">Например, если свойство **коммуникатионмоде** имеет значение Phone, то это свойство указывает номер телефона для вызова.</span><span class="sxs-lookup"><span data-stu-id="01c0b-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="01c0b-121">**коммуникатионмоде**</span><span class="sxs-lookup"><span data-stu-id="01c0b-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01c0b-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01c0b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-124">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Поддержка DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="01c0b-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-125">Форма взаимодействия, используемая для получения поддержки.</span><span class="sxs-lookup"><span data-stu-id="01c0b-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01c0b-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="01c0b-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="01c0b-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Телефон** (2)</span><span class="sxs-lookup"><span data-stu-id="01c0b-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="01c0b-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Факс** (3)</span><span class="sxs-lookup"><span data-stu-id="01c0b-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="01c0b-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span><span class="sxs-lookup"><span data-stu-id="01c0b-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="01c0b-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Веб-служба** (5)</span><span class="sxs-lookup"><span data-stu-id="01c0b-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="01c0b-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Веб-страница** (6)</span><span class="sxs-lookup"><span data-stu-id="01c0b-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="01c0b-132">Веб-страница</span><span class="sxs-lookup"><span data-stu-id="01c0b-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="01c0b-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span><span class="sxs-lookup"><span data-stu-id="01c0b-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="01c0b-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Электронная почта** (8)</span><span class="sxs-lookup"><span data-stu-id="01c0b-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="01c0b-135">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="01c0b-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01c0b-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01c0b-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="01c0b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01c0b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Поддержка DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="01c0b-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-140">Текстовое описание предоставляемого типа поддержки.</span><span class="sxs-lookup"><span data-stu-id="01c0b-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="01c0b-141">**Локаль**</span><span class="sxs-lookup"><span data-stu-id="01c0b-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="01c0b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01c0b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Поддержка DMTF \| 001,2 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01c0b-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-145">Географический регион или диалект языка, к которому относится этот ресурс поддержки.</span><span class="sxs-lookup"><span data-stu-id="01c0b-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="01c0b-146">**суппортакцессид**</span><span class="sxs-lookup"><span data-stu-id="01c0b-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="01c0b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01c0b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-149">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01c0b-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-150">Произвольная строка произвольной формы, определяемая поставщиком продукта или организацией, которая развертывает продукт.</span><span class="sxs-lookup"><span data-stu-id="01c0b-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="01c0b-151">Это свойство, поскольку оно является ключом, должно быть уникальным в рамках всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="01c0b-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01c0b-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01c0b-152">Remarks</span></span>

<span data-ttu-id="01c0b-153">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="01c0b-153">WMI does not implement this class.</span></span>

<span data-ttu-id="01c0b-154">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="01c0b-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01c0b-155">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="01c0b-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c0b-156">Требования</span><span class="sxs-lookup"><span data-stu-id="01c0b-156">Requirements</span></span>



| <span data-ttu-id="01c0b-157">Требование</span><span class="sxs-lookup"><span data-stu-id="01c0b-157">Requirement</span></span> | <span data-ttu-id="01c0b-158">Значение</span><span class="sxs-lookup"><span data-stu-id="01c0b-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01c0b-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01c0b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="01c0b-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01c0b-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01c0b-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01c0b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="01c0b-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01c0b-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01c0b-163">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="01c0b-163">Namespace</span></span><br/>                | <span data-ttu-id="01c0b-164">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="01c0b-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01c0b-165">MOF</span><span class="sxs-lookup"><span data-stu-id="01c0b-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01c0b-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01c0b-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01c0b-167">DLL</span><span class="sxs-lookup"><span data-stu-id="01c0b-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01c0b-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c0b-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

