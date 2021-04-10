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
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>мбнпрофиликст

Элемент **мбнпрофиликст** является расширением более раннего элемента мбнпрофиле. Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.

В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий. Используйте дочерний элемент [**профилекондитионедон**](element-profileconditionedon.md) из **мбнпрофиликст** , чтобы указать, какие операционные условия делают определенный профиль активным.

## <a name="element-hierarchy"></a>Иерархия элементов

**<MBNProfileExt>**

## <a name="syntax"></a>Синтаксис

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

### <a name="key"></a>Ключ

`?`   необязательно (ноль или один)

`*`   необязательно (ноль или более)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Нет.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Дочерний элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-adminenable.md">админенабле</a></td>
<td><p>Указывает, включен ли профиль в административном состоянии. Это новый элемент для v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-adminroamcontrol.md">админроамконтрол</a></td>
<td><p>Указывает, управляется ли профиль административным роумингом. Этот элемент является новым для v4. Значением этого элемента является значение <a href="simpletype-roamcontroltype.md"><strong>роамконтролтипе</strong></a> . Это необязательный элемент. Если значение не указано, по умолчанию используется <strong>аллроамалловед</strong> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-apnid.md">апнид</a></td>
<td><p>Идентификатор APN, связанный с этим профилем. Этот элемент является новым в v4 и является необязательным.</p></td>
</tr>
<tr class="even">
<td><a href="element-autoconnectoninternet.md">аутоконнектонинтернет</a></td>
<td><p>Указывает, будет ли устройство мобильной широкополосной связи автоматически подключаться к сети.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>аутоконнектонинтернет</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-connectionmode.md">ConnectionMode</a></td>
<td><p>Задает параметр автоматического подключения, используемый для устройства мобильной широкополосной связи.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-context.md">Контекст</a></td>
<td><p>Задает параметры, необходимые для установления подключения к данным.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Указывает список предпочтительных поставщиков сети при роуминге.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>датароамингпартнерс</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-description.md">Описание</a></td>
<td><p>Описание профиля.</p></td>
</tr>
<tr class="odd">
<td><a href="element-homeprovidername.md">HomeProviderName</a></td>
<td><p>Имя поставщика услуг домашнего доступа для указанной SIM-карты или устройства. Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>хомепровидернаме</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-iconfilepath.md">иконфилепас</a></td>
<td><p>Путь к файлу значка для соединения. Пользовательский интерфейс подключения операционной системы отображает значок, когда подключение устанавливается с помощью этого профиля.</p>
<p>Дополнительные сведения об использовании этого элемента см. в документации по версии 1 для <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>иконфилепас</strong></a>.</p></td>
</tr>
<tr class="odd">
<td><a href="element-isdefault.md">IsDefault</a></td>
<td><p>Указывает, является ли этот профиль профилем по умолчанию.</p>
<p>Дополнительные сведения об этом элементе см. в документации по параметру <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>Default</strong></a>.</p></td>
</tr>
<tr class="even">
<td><a href="element-isexclusivetoother.md">исексклусиветусер</a></td>
<td><p>Указывает, что этот профиль является эксклюзивным для других профилей того же набора профилей. Этот элемент является новым для v4.</p></td>
</tr>
<tr class="odd">
<td><a href="element-islongstandingadditionalpdpcontextprofile.md">ислонгстандингаддитионалпдпконтекстпрофиле</a></td>
<td><p>Указывает, что этот профиль является долгосрочным дополнительным профилем контекста PDP. Если значение этого элемента равно <strong>true</strong>, то для <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> также должно быть задано значение <strong>true</strong>. Это новый элемент для v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-isprovisioningprofile.md">испровисионингпрофиле</a></td>
<td><p>Указывает, что этот профиль должен использоваться только для подготовки. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP). Этот элемент является новым для v4.</p>
<p>Если <strong>испровисионингпрофиле</strong> имеет значение true, то значение <a href="element-isdefault.md"><strong>по умолчанию</strong></a> должно быть равно false, а <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> — вручную.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmsconfiguration.md">ммсконфигуратион</a></td>
<td><p>Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</p>
<p>Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</p>
<ul>
<li>Его элемент <a href="element-name.md"><strong>Name</strong></a> должен содержать уникальное для всей системы имя.</li>
<li>Его <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> должен быть установлен в значение <strong>усерпровисионед</strong>.</li>
<li>Его <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</li>
<li>Его <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> должен быть установлен в значение " <strong>вручную</strong>".</li>
<li>Его <a href="element-purposegroupguid.md"><strong>пурпосеграупгуид</strong></a> должен содержать GUID для группы целей MMS.</li>
<li>Его <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> должен быть установлен в <strong>значение true</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="element-name.md">имя</a>;</td>
<td><p>Имя профиля. Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-name-mbnprofile-element.md"><strong>имени</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-profileconditionedon.md">профилекондитионедон</a></td>
<td><p>Указывает условия, которые должны быть удовлетворены для применения профиля.</p>
<p>Этот элемент является новым для v4. Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля. Этот элемент является необязательным. Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</p></td>
</tr>
<tr class="even">
<td><a href="element-profilecreationtype.md">Профилекреатионтипе (в Мбнпрофиликст)</a></td>
<td><p>Указывает создателя профиля.</p>
<p>Дополнительные сведения об этом элементе см. в документации по элементу <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-purposegroups.md">пурпосеграупс</a></td>
<td><p>Необязательный список групп профилей, где каждая группа включает профили, используемые для общего назначения.</p>
<p>Этот элемент является новым для V4 схемы.</p>
<p>Один профиль может быть указан в нескольких группах.</p></td>
</tr>
<tr class="even">
<td><a href="element-simiccid.md">симикЦид</a></td>
<td><p>Номер Идентифкатион SIM для устройств GSM. Дополнительные сведения см. в документации по элементу <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-subscriberid.md">субскриберид</a></td>
<td><p>Определяет уникальный идентификатор профиля.</p>
<p>Для сети GSM оно должно содержать IMSI (Международный идентификатор мобильного подписчика) SIM-карты и устройства CDMA, которые должны содержать минимальное значение (мобильный идентификационный номер) устройства.</p>
<p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>субскриберид</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы

Этот внешний элемент (Document) не может содержаться в каких-либо других элементах.

## <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Пространство имен</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
