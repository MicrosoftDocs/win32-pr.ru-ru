---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343782"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="f89af-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>мбнпрофиликст</span><span class="sxs-lookup"><span data-stu-id="f89af-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="f89af-104">Элемент **мбнпрофиликст** является расширением более раннего элемента мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="f89af-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="f89af-105">Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</span><span class="sxs-lookup"><span data-stu-id="f89af-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="f89af-106">В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий.</span><span class="sxs-lookup"><span data-stu-id="f89af-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="f89af-107">Используйте дочерний элемент [**профилекондитионедон**](element-profileconditionedon.md) из **мбнпрофиликст** , чтобы указать, какие операционные условия делают определенный профиль активным.</span><span class="sxs-lookup"><span data-stu-id="f89af-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f89af-108">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="f89af-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="f89af-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f89af-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="f89af-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="f89af-110">Key</span></span>

<span data-ttu-id="f89af-111">`?`   необязательно (ноль или один)</span><span class="sxs-lookup"><span data-stu-id="f89af-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="f89af-112">`*`   необязательно (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="f89af-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f89af-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="f89af-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f89af-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f89af-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f89af-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="f89af-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f89af-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f89af-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f89af-117">Дочерний элемент</span><span class="sxs-lookup"><span data-stu-id="f89af-117">Child Element</span></span></th>
<th><span data-ttu-id="f89af-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f89af-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f89af-119"><a href="element-adminenable.md">админенабле</a></span><span class="sxs-lookup"><span data-stu-id="f89af-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="f89af-120">Указывает, включен ли профиль в административном состоянии. Это новый элемент для v4.</span><span class="sxs-lookup"><span data-stu-id="f89af-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-121"><a href="element-adminroamcontrol.md">админроамконтрол</a></span><span class="sxs-lookup"><span data-stu-id="f89af-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="f89af-122">Указывает, управляется ли профиль административным роумингом.</span><span class="sxs-lookup"><span data-stu-id="f89af-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="f89af-123">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="f89af-123">This element is new for v4.</span></span> <span data-ttu-id="f89af-124">Значением этого элемента является значение <a href="simpletype-roamcontroltype.md"><strong>роамконтролтипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f89af-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="f89af-125">Это необязательный элемент. Если значение не указано, по умолчанию используется <strong>аллроамалловед</strong> .</span><span class="sxs-lookup"><span data-stu-id="f89af-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-126"><a href="element-apnid.md">апнид</a></span><span class="sxs-lookup"><span data-stu-id="f89af-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="f89af-127">Идентификатор APN, связанный с этим профилем. Этот элемент является новым в v4 и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f89af-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-128"><a href="element-autoconnectoninternet.md">аутоконнектонинтернет</a></span><span class="sxs-lookup"><span data-stu-id="f89af-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="f89af-129">Указывает, будет ли устройство мобильной широкополосной связи автоматически подключаться к сети.</span><span class="sxs-lookup"><span data-stu-id="f89af-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="f89af-130">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>аутоконнектонинтернет</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="f89af-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="f89af-132">Задает параметр автоматического подключения, используемый для устройства мобильной широкополосной связи.</span><span class="sxs-lookup"><span data-stu-id="f89af-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="f89af-133">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-134"><a href="element-context.md">Контекст</a></span><span class="sxs-lookup"><span data-stu-id="f89af-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="f89af-135">Задает параметры, необходимые для установления подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="f89af-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="f89af-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="f89af-137">Указывает список предпочтительных поставщиков сети при роуминге.</span><span class="sxs-lookup"><span data-stu-id="f89af-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="f89af-138">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>датароамингпартнерс</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-139"><a href="element-description.md">Описание</a></span><span class="sxs-lookup"><span data-stu-id="f89af-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="f89af-140">Описание профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="f89af-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="f89af-142">Имя поставщика услуг домашнего доступа для указанной SIM-карты или устройства.</span><span class="sxs-lookup"><span data-stu-id="f89af-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="f89af-143">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>хомепровидернаме</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-144"><a href="element-iconfilepath.md">иконфилепас</a></span><span class="sxs-lookup"><span data-stu-id="f89af-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="f89af-145">Путь к файлу значка для соединения.</span><span class="sxs-lookup"><span data-stu-id="f89af-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="f89af-146">Пользовательский интерфейс подключения операционной системы отображает значок, когда подключение устанавливается с помощью этого профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="f89af-147">Дополнительные сведения об использовании этого элемента см. в документации по версии 1 для <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>иконфилепас</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f89af-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="f89af-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="f89af-149">Указывает, является ли этот профиль профилем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f89af-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="f89af-150">Дополнительные сведения об этом элементе см. в документации по параметру <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>Default</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f89af-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-151"><a href="element-isexclusivetoother.md">исексклусиветусер</a></span><span class="sxs-lookup"><span data-stu-id="f89af-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="f89af-152">Указывает, что этот профиль является эксклюзивным для других профилей того же набора профилей. Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="f89af-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">ислонгстандингаддитионалпдпконтекстпрофиле</a></span><span class="sxs-lookup"><span data-stu-id="f89af-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="f89af-154">Указывает, что этот профиль является долгосрочным дополнительным профилем контекста PDP. Если значение этого элемента равно <strong>true</strong>, то для <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> также должно быть задано значение <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="f89af-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="f89af-155">Это новый элемент для v4.</span><span class="sxs-lookup"><span data-stu-id="f89af-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-156"><a href="element-isprovisioningprofile.md">испровисионингпрофиле</a></span><span class="sxs-lookup"><span data-stu-id="f89af-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="f89af-157">Указывает, что этот профиль должен использоваться только для подготовки. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).</span><span class="sxs-lookup"><span data-stu-id="f89af-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="f89af-158">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="f89af-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="f89af-159">Если <strong>испровисионингпрофиле</strong> имеет значение true, то значение <a href="element-isdefault.md"><strong>по умолчанию</strong></a> должно быть равно false, а <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> — вручную.</span><span class="sxs-lookup"><span data-stu-id="f89af-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-160"><a href="element-mmsconfiguration.md">ммсконфигуратион</a></span><span class="sxs-lookup"><span data-stu-id="f89af-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="f89af-161">Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</span><span class="sxs-lookup"><span data-stu-id="f89af-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="f89af-162">Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f89af-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="f89af-163">Его элемент <a href="element-name.md"><strong>Name</strong></a> должен содержать уникальное для всей системы имя.</span><span class="sxs-lookup"><span data-stu-id="f89af-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="f89af-164">Его <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> должен быть установлен в значение <strong>усерпровисионед</strong>.</span><span class="sxs-lookup"><span data-stu-id="f89af-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="f89af-165">Его <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</span><span class="sxs-lookup"><span data-stu-id="f89af-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="f89af-166">Его <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> должен быть установлен в значение " <strong>вручную</strong>".</span><span class="sxs-lookup"><span data-stu-id="f89af-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="f89af-167">Его <a href="element-purposegroupguid.md"><strong>пурпосеграупгуид</strong></a> должен содержать GUID для группы целей MMS.</span><span class="sxs-lookup"><span data-stu-id="f89af-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="f89af-168">Его <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> должен быть установлен в <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="f89af-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-169"><a href="element-name.md">имя</a>;</span><span class="sxs-lookup"><span data-stu-id="f89af-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="f89af-170">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-170">The name of the profile.</span></span> <span data-ttu-id="f89af-171">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-name-mbnprofile-element.md"><strong>имени</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-172"><a href="element-profileconditionedon.md">профилекондитионедон</a></span><span class="sxs-lookup"><span data-stu-id="f89af-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="f89af-173">Указывает условия, которые должны быть удовлетворены для применения профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="f89af-174">Этот элемент является новым для v4.</span><span class="sxs-lookup"><span data-stu-id="f89af-174">This element is new for v4.</span></span> <span data-ttu-id="f89af-175">Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="f89af-176">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f89af-176">This element is optional.</span></span> <span data-ttu-id="f89af-177">Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="f89af-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-178"><a href="element-profilecreationtype.md">Профилекреатионтипе (в Мбнпрофиликст)</a></span><span class="sxs-lookup"><span data-stu-id="f89af-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="f89af-179">Указывает создателя профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="f89af-180">Дополнительные сведения об этом элементе см. в документации по элементу <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-181"><a href="element-purposegroups.md">пурпосеграупс</a></span><span class="sxs-lookup"><span data-stu-id="f89af-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="f89af-182">Необязательный список групп профилей, где каждая группа включает профили, используемые для общего назначения.</span><span class="sxs-lookup"><span data-stu-id="f89af-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="f89af-183">Этот элемент является новым для V4 схемы.</span><span class="sxs-lookup"><span data-stu-id="f89af-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="f89af-184">Один профиль может быть указан в нескольких группах.</span><span class="sxs-lookup"><span data-stu-id="f89af-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f89af-185"><a href="element-simiccid.md">симикЦид</a></span><span class="sxs-lookup"><span data-stu-id="f89af-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="f89af-186">Номер Идентифкатион SIM для устройств GSM.</span><span class="sxs-lookup"><span data-stu-id="f89af-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="f89af-187">Дополнительные сведения см. в документации по элементу <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f89af-188"><a href="element-subscriberid.md">субскриберид</a></span><span class="sxs-lookup"><span data-stu-id="f89af-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="f89af-189">Определяет уникальный идентификатор профиля.</span><span class="sxs-lookup"><span data-stu-id="f89af-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="f89af-190">Для сети GSM оно должно содержать IMSI (Международный идентификатор мобильного подписчика) SIM-карты и устройства CDMA, которые должны содержать минимальное значение (мобильный идентификационный номер) устройства.</span><span class="sxs-lookup"><span data-stu-id="f89af-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="f89af-191">Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>субскриберид</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="f89af-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f89af-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f89af-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="f89af-193">Этот внешний элемент (Document) не может содержаться в каких-либо других элементах.</span><span class="sxs-lookup"><span data-stu-id="f89af-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="f89af-194">Требования</span><span class="sxs-lookup"><span data-stu-id="f89af-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f89af-195">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f89af-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
