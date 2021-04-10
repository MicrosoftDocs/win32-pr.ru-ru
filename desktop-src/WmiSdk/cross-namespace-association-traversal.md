---
description: Начиная с Windows 7, инструментарий управления Windows (WMI) (WMI) реализовали стандартный механизм для обнаружения профилей с помощью схемы CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Просмотр связей между пространствами имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898797"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="81151-103">Просмотр связей между пространствами имен</span><span class="sxs-lookup"><span data-stu-id="81151-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="81151-104">Начиная с Windows 7, инструментарий управления Windows (WMI) (WMI) реализовали стандартный механизм для обнаружения профилей с помощью схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="81151-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="81151-105">Инструментарий WMI поддерживает регистрацию связей между пространствами имен и сопоставление профилей взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="81151-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="81151-106">Дополнительные сведения о регистрации профилей и реализации CIM для обхода ассоциации см. в разделе DSP1033 (). [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf)</span><span class="sxs-lookup"><span data-stu-id="81151-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="81151-107">Для поддержки этой функции инфраструктура WMI выполнила следующие действия:</span><span class="sxs-lookup"><span data-stu-id="81151-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="81151-108">Создано пространство имен взаимодействия: \\ корневое \\ взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="81151-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="81151-109">Разрешено прохождение сопоставления между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="81151-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="81151-110">Ассоциации, которые пересекают пространства имен, поддерживают фильтрацию на уровне класса ассоциации и на уровне реализованного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="81151-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="81151-111">Добавлены классы [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)и [**CIM \_ референцедпрофиле**](cim-referencedprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="81151-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="81151-112">Реализована совместимость схемы CIM версии 2.17.1.</span><span class="sxs-lookup"><span data-stu-id="81151-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="81151-113">Дополнительные сведения см. в разделе [Совместимость схемы CIM](cim-schema-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="81151-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="81151-114">Пространство имен Interop</span><span class="sxs-lookup"><span data-stu-id="81151-114">Interop Namespace</span></span>

<span data-ttu-id="81151-115">Пространство имен Interop предоставляет клиентским приложениям общее расположение для обнаружения всех профилей, поддерживаемых на компьютере.</span><span class="sxs-lookup"><span data-stu-id="81151-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="81151-116">Профили можно использовать для управления различными аспектами операционной системы, массива хранения или базы данных.</span><span class="sxs-lookup"><span data-stu-id="81151-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="81151-117">Все классы взаимодействия и объекты должны быть определены в корневом \\ пространстве имен взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="81151-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="81151-118">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="81151-118">CIM Classes</span></span>

<span data-ttu-id="81151-119">Классы CIM, описанные в следующем списке, поддерживают обход взаимосвязей между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="81151-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="81151-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_РЕГИСТЕРЕДПРОФИЛЕ CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81151-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="81151-121">Используется для определения спецификации профиля, объявленной как реализованная.</span><span class="sxs-lookup"><span data-stu-id="81151-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="81151-122">Этот класс задает сведения, включающие имя профиля, организацию и версию, с которыми совместима реализация.</span><span class="sxs-lookup"><span data-stu-id="81151-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="81151-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ЕЛЕМЕНТКОНФОРМСТОПРОФИЛЕ CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="81151-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="81151-124">Используется для связывания экземпляров элементов управления, определенных в профилях, с классом [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) , который определяет определенные спецификации профиля, которые реализуются.</span><span class="sxs-lookup"><span data-stu-id="81151-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="81151-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_РЕФЕРЕНЦЕДПРОФИЛЕ CIM**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="81151-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="81151-126">Используется для представления связи между профилями.</span><span class="sxs-lookup"><span data-stu-id="81151-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="81151-127">Реализация обхода связей между пространствами имен</span><span class="sxs-lookup"><span data-stu-id="81151-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="81151-128">Служба WMI разрешает прохождение связей между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="81151-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="81151-129">Инструментарий WMI предоставляет пространство имен взаимодействия для регистрации профилей и связывания их с профилями, реализованными в разных пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="81151-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="81151-130">Однако, чтобы использовать обход ассоциаций, разработчики должны создать экземпляры классов профилей как в Interop, так и в реализованном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="81151-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="81151-131">Дополнительные сведения см. в разделе [запись поставщика взаимосвязей для взаимодействия](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="81151-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="81151-132">Ассоциации, которые пересекают пространства имен в одной среде управления, должны создаваться как в взаимодействии, так и в реализованных пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="81151-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="81151-133">В противном случае обход связи не будет работать.</span><span class="sxs-lookup"><span data-stu-id="81151-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="81151-134">Например, поставщик сопоставления профилей управления питанием должен быть зарегистрирован как с корневым, так и с использованием пространств имен root/cimv2/Power.</span><span class="sxs-lookup"><span data-stu-id="81151-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="81151-135">Обход взаимосвязей должен осуществляться из любого пространства имен обратно в другое.</span><span class="sxs-lookup"><span data-stu-id="81151-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="81151-136">Примеры обхода связей см. [в разделе доступ к данным в пространстве имен Interop](accessing-data-in-the-interop-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="81151-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="81151-137">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="81151-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="81151-138">После обновления до Windows 7 при наличии профилей устройств взаимодействия, которые ранее были установлены в пространстве имен root или Interop, профили Windows 7 не будут установлены.</span><span class="sxs-lookup"><span data-stu-id="81151-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="81151-139">Эти сторонние объекты профиля перезапишут схему взаимодействия Windows 7 для поддержки функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="81151-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="81151-140">Кроме того, регистрируется событие с ИДЕНТИФИКАТОРом 5631 приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="81151-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="81151-141">Чтобы получить профили взаимодействия Windows 7, необходимо скомпилировать версию Windows 7 файла Interop. mof и соответствующие файлы МФЛ.</span><span class="sxs-lookup"><span data-stu-id="81151-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="81151-142">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="81151-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81151-143">См. также</span><span class="sxs-lookup"><span data-stu-id="81151-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="81151-144">[**\_РЕГИСТЕРЕДПРОФИЛЕ CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81151-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="81151-145">**\_ЕЛЕМЕНТКОНФОРМСТОПРОФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="81151-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="81151-146">**\_РЕФЕРЕНЦЕДПРОФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="81151-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="81151-147">Совместимость со схемой CIM</span><span class="sxs-lookup"><span data-stu-id="81151-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="81151-148">Написание поставщика ассоциаций для взаимодействия</span><span class="sxs-lookup"><span data-stu-id="81151-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="81151-149">Доступ к данным в пространстве имен Interop</span><span class="sxs-lookup"><span data-stu-id="81151-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
