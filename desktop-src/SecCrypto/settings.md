---
description: Используется для настройки компонентов CAPICOM.
title: Объект параметров
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689010"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="730b3-103">Объект Settings (криптография)</span><span class="sxs-lookup"><span data-stu-id="730b3-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="730b3-104">\[Объект **параметров** доступен для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="730b3-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="730b3-105">Объект **параметров** используется для настройки компонентов CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="730b3-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="730b3-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="730b3-106">Members</span></span>

<span data-ttu-id="730b3-107">Объект **параметров** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="730b3-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="730b3-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="730b3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="730b3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="730b3-109">Properties</span></span>

<span data-ttu-id="730b3-110">Объект **параметров** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="730b3-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="730b3-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="730b3-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="730b3-112">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="730b3-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="730b3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="730b3-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="730b3-114"><a href="settings-activedirectorysearchlocation.md"><strong>активедиректорисеарчлокатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="730b3-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="730b3-115">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="730b3-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="730b3-116">Задает или получает расположение поиска Active Directory.</span><span class="sxs-lookup"><span data-stu-id="730b3-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="730b3-117">По умолчанию начальное расположение не указано.</span><span class="sxs-lookup"><span data-stu-id="730b3-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="730b3-118">Если расположение не указано, выполняется поиск в глобальном каталоге, а затем выполняется поиск по домену по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="730b3-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="730b3-119">Поиск определяет, опубликован ли атрибут сертификата пользователя в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="730b3-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="730b3-120"><a href="settings-enablepromptforcertificateui.md"><strong>енаблепромптфорцертификатеуи</strong></a></span><span class="sxs-lookup"><span data-stu-id="730b3-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="730b3-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="730b3-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="730b3-122">Задает или получает логическое значение, указывающее, можно ли использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя.</span><span class="sxs-lookup"><span data-stu-id="730b3-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="730b3-123">Задание этого свойства не отключает предупреждения, которые генерируются до того, как использование закрытого ключа выполняется из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="730b3-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="730b3-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="730b3-124">Remarks</span></span>

<span data-ttu-id="730b3-125">Объект **параметров** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="730b3-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="730b3-126">ProgID для объекта **параметров** — CAPICOM. Settings. 1.</span><span class="sxs-lookup"><span data-stu-id="730b3-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="730b3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="730b3-127">Requirements</span></span>



| <span data-ttu-id="730b3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="730b3-128">Requirement</span></span> | <span data-ttu-id="730b3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="730b3-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="730b3-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="730b3-130">Redistributable</span></span><br/> | <span data-ttu-id="730b3-131">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="730b3-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="730b3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="730b3-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="730b3-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="730b3-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="730b3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="730b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730b3-135">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="730b3-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




