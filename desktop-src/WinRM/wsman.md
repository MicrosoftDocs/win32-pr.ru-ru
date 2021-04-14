---
title: Объект WSMan (Всмандисп. h)
description: Предоставляет методы и свойства, используемые для создания сеанса, представленного объектом Session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Объект WSMan служба удаленного управления Windows
- Объект WSMan служба удаленного управления Windows, описание
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414877"
---
# <a name="wsman-object"></a><span data-ttu-id="7cd65-105">Объект WSMan</span><span class="sxs-lookup"><span data-stu-id="7cd65-105">WSMan object</span></span>

<span data-ttu-id="7cd65-106">Предоставляет методы и свойства, используемые для создания сеанса, представленного объектом [**Session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd65-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="7cd65-107">Любой служба удаленного управления Windows операции требует создания [**сеанса**](session.md) , который подключается к удаленному компьютеру, [*базовому контроллеру управления*](windows-remote-management-glossary.md) (BMC) или локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="7cd65-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="7cd65-108">К операциям относятся получение, запись, перечисление или вызов методов.</span><span class="sxs-lookup"><span data-stu-id="7cd65-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="7cd65-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="7cd65-109">Members</span></span>

<span data-ttu-id="7cd65-110">Объект **WSMan** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7cd65-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="7cd65-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7cd65-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7cd65-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7cd65-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7cd65-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7cd65-113">Methods</span></span>

<span data-ttu-id="7cd65-114">Объект **WSMan** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7cd65-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7cd65-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7cd65-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7cd65-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7cd65-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-117"><a href="wsman-createconnectionoptions.md"><strong>креатеконнектионоптионс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-118">Создает объект <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> , который указывает имя пользователя и пароль, используемые при создании удаленного сеанса.</span><span class="sxs-lookup"><span data-stu-id="7cd65-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-119"><a href="wsman-createresourcelocator.md"><strong>креатересаурцелокатор</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-120">Создает объект <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> , который может указывать:</span><span class="sxs-lookup"><span data-stu-id="7cd65-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="7cd65-121">Полный путь к <a href="windows-remote-management-glossary.md"><em>ресурсу</em></a> или отдельному фрагменту данных.</span><span class="sxs-lookup"><span data-stu-id="7cd65-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="7cd65-122"><a href="windows-remote-management-glossary.md"><em>Селектор</em></a> для конкретного экземпляра ресурса.</span><span class="sxs-lookup"><span data-stu-id="7cd65-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="7cd65-123"><a href="windows-remote-management-glossary.md"><em>Параметр</em></a> , предоставляющий дополнительные данные поставщику ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cd65-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-125">Создает объект <a href="session.md"><strong>сеанса</strong></a> , который затем может использоваться для последующих сетевых операций.</span><span class="sxs-lookup"><span data-stu-id="7cd65-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. Енумератионфлагхиерарчидип</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-127">Возвращает значение флага перечисления <strong>енумератионфлагхиерарчидип</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. Енумератионфлагхиерарчидипбасепропсонли</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-129">Возвращает значение флага перечисления <strong>енумератионфлагхиерарчидипбасепропсонли</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. Енумератионфлагхиерарчишаллов</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-131">Возвращает значение флага перечисления <strong>енумератионфлагхиерарчишаллов</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. Енумератионфлагнонксмлтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-133">Возвращает значение константы перечисления <strong>всманфлагнонксмлтекст</strong> для использования в параметре <em>flags</em> метода <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cd65-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. Енумератионфлагретурнепр</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-135">Возвращает значение флага перечисления <strong>енумератионфлагретурнепр</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. Енумератионфлагретурнобжект</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-137">Возвращает значение флага перечисления <strong>енумератионфлагретурнобжект</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. Енумератионфлагретурнобжектандепр</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-139">Возвращает значение флага перечисления <strong>енумератионфлагретурнобжектандепр</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-140"><a href="wsman-geterrormessage.md"><strong>WSMan. Жетеррормессаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-141">Возвращает отформатированную строку, содержащую текст номера ошибки.</span><span class="sxs-lookup"><span data-stu-id="7cd65-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. Сессионфлагкредусернамепассворд</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-143">Возвращает значение флага проверки подлинности <strong>всманфлагкредусернамепассворд</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. Сессионфлаженаблеспнсерверпорт</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-145">Возвращает значение флага проверки подлинности <strong>всманфлаженаблеспнсерверпорт</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. Сессионфлагноенкриптион</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-147">Возвращает значение флага проверки подлинности <strong>всманфлагноенкриптион</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. Сессионфлагскипкачекк</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-149">Возвращает значение флага проверки подлинности <strong>всманфлагскипкачекк</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. Сессионфлагскипкнчекк</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-151">Возвращает значение флага проверки подлинности <strong>всманфлагскипкнчекк</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. Сессионфлагусебасик</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-153">Возвращает значение флага проверки подлинности <strong>всманфлагусебасик</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. Сессионфлагуседижест</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-155">Возвращает значение флага проверки подлинности <strong>всманфлагуседижест</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. Сессионфлагусекерберос</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-157">Возвращает значение флага проверки подлинности <strong>всманфлагусекерберос</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. Сессионфлагусенеготиате</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-159">Возвращает значение флага проверки подлинности <strong>всманфлагусенеготиате</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7cd65-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. Сессионфлагусеноаусентикатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-161">Возвращает значение флага проверки подлинности <strong>всманфлагусеноаусентикатион</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7cd65-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cd65-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="7cd65-163">Возвращает значение флага проверки подлинности <strong>WSManFlagUTF8</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7cd65-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="7cd65-164">Свойства</span><span class="sxs-lookup"><span data-stu-id="7cd65-164">Properties</span></span>

<span data-ttu-id="7cd65-165">Объект **WSMan** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7cd65-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="7cd65-166">Свойство</span><span class="sxs-lookup"><span data-stu-id="7cd65-166">Property</span></span>                                            | <span data-ttu-id="7cd65-167">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7cd65-167">Access type</span></span>          | <span data-ttu-id="7cd65-168">Описание</span><span class="sxs-lookup"><span data-stu-id="7cd65-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="7cd65-169">**Команд**</span><span class="sxs-lookup"><span data-stu-id="7cd65-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="7cd65-170">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7cd65-170">Read-only</span></span><br/> | <span data-ttu-id="7cd65-171">Возвращает необработанную командную строку для текущего ведущего процесса.</span><span class="sxs-lookup"><span data-stu-id="7cd65-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="7cd65-172">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="7cd65-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="7cd65-173">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7cd65-173">Read-only</span></span><br/> | <span data-ttu-id="7cd65-174">Возвращает сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7cd65-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="7cd65-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cd65-175">Remarks</span></span>

<span data-ttu-id="7cd65-176">Объект **WSMan** соответствует интерфейсам [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) и [**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) .</span><span class="sxs-lookup"><span data-stu-id="7cd65-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="7cd65-177">**WSMan** — это единственный объект, который можно создать напрямую с помощью функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7cd65-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="7cd65-178">Примеры</span><span class="sxs-lookup"><span data-stu-id="7cd65-178">Examples</span></span>

<span data-ttu-id="7cd65-179">В следующем примере кода показано, как создать экземпляр объекта **WSMan** .</span><span class="sxs-lookup"><span data-stu-id="7cd65-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="7cd65-180">Требования</span><span class="sxs-lookup"><span data-stu-id="7cd65-180">Requirements</span></span>



| <span data-ttu-id="7cd65-181">Требование</span><span class="sxs-lookup"><span data-stu-id="7cd65-181">Requirement</span></span> | <span data-ttu-id="7cd65-182">Значение</span><span class="sxs-lookup"><span data-stu-id="7cd65-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd65-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cd65-183">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd65-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cd65-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7cd65-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cd65-185">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd65-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cd65-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7cd65-187">Header</span><span class="sxs-lookup"><span data-stu-id="7cd65-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd65-188"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd65-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cd65-189">IDL</span><span class="sxs-lookup"><span data-stu-id="7cd65-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7cd65-190"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cd65-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7cd65-191">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7cd65-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cd65-192"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cd65-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cd65-193">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd65-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd65-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd65-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7cd65-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cd65-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd65-196">API сценариев WinRM</span><span class="sxs-lookup"><span data-stu-id="7cd65-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="7cd65-197">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="7cd65-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="7cd65-198">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="7cd65-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="7cd65-199">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="7cd65-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="7cd65-200">Получение данных с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="7cd65-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="7cd65-201">Получение данных с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="7cd65-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

