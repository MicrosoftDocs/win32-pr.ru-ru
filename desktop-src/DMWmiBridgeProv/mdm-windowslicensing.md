---
title: Класс MDM_WindowsLicensing
description: Класс MDM \_ виндовслиценсинг предназначен для сценариев управления, связанных с лицензированием.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Класс MDM_WindowsLicensing
- MDM_WindowsLicensing класс, описание
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654475"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="08175-105">\_Класс MDM виндовслиценсинг</span><span class="sxs-lookup"><span data-stu-id="08175-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="08175-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="08175-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08175-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="08175-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08175-108">Класс **MDM \_ виндовслиценсинг** предназначен для сценариев управления, связанных с лицензированием.</span><span class="sxs-lookup"><span data-stu-id="08175-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="08175-109">В настоящее время область ограничена обновлением выпуска Windows 10 Desktop и мобильными устройствами, например Windows 10 Pro до Windows 10 Корпоративная.</span><span class="sxs-lookup"><span data-stu-id="08175-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="08175-110">Кроме того, этот CSP предоставляет возможность активировать или изменить ключ продукта для устройств Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="08175-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="08175-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="08175-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08175-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08175-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="08175-113">Члены</span><span class="sxs-lookup"><span data-stu-id="08175-113">Members</span></span>

<span data-ttu-id="08175-114">Класс **MDM \_ виндовслиценсинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="08175-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="08175-115">Методы</span><span class="sxs-lookup"><span data-stu-id="08175-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="08175-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="08175-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08175-117">Методы</span><span class="sxs-lookup"><span data-stu-id="08175-117">Methods</span></span>

<span data-ttu-id="08175-118">Класс **MDM \_ виндовслиценсинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="08175-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="08175-119">Метод</span><span class="sxs-lookup"><span data-stu-id="08175-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="08175-120">Описание</span><span class="sxs-lookup"><span data-stu-id="08175-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="08175-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>чанжепродукткэймесод</strong></a></span><span class="sxs-lookup"><span data-stu-id="08175-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="08175-122">Устанавливает ключ продукта для устройств Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="08175-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="08175-123">Не выполняет перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="08175-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="08175-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>чеккаппликабилитимесод</strong></a></span><span class="sxs-lookup"><span data-stu-id="08175-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="08175-125">Метод, позволяющий проверить, можно ли использовать указанный ключ продукта для обновления выпуска, активировать или изменить ключ продукта Windows 10 для настольных устройств.</span><span class="sxs-lookup"><span data-stu-id="08175-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="08175-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>упградидитионвислиценсемесод</strong></a></span><span class="sxs-lookup"><span data-stu-id="08175-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="08175-127">Предоставьте лицензию на обновление выпуска для устройств Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="08175-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08175-128">Этот процесс обновления не требует перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="08175-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="08175-129">Тип даты — XML.</span><span class="sxs-lookup"><span data-stu-id="08175-129">The date type is XML.</span></span><br/> <span data-ttu-id="08175-130">Поддерживаемая операция — Execute.</span><span class="sxs-lookup"><span data-stu-id="08175-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="08175-131">Содержимое файла лицензии XML должно быть правильно экранировано (то есть он не должен быть просто копированием XML); в противном случае обновление выпуска на устройствах Windows 10 Mobile завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="08175-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="08175-132">Дополнительные сведения о правильном экранировании XML-файла лицензии см. в разделе 2,4 <a href="https://www.w3.org/TR/xml/">спецификации W3C XML</a>. Файл лицензии XML получен из центра поддержки корпоративных лицензий Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="08175-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="08175-133">Чтобы получить доступ к порталу, ваша организация должна иметь контракт корпоративного лицензирования с корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="08175-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="08175-134">Ниже приведены допустимые варианты обновления выпуска при использовании этого узла с помощью пакета MDM или подготовки.</span><span class="sxs-lookup"><span data-stu-id="08175-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="08175-135">Windows 10 Мобилето Windows 10 Mobile Корпоративная</span><span class="sxs-lookup"><span data-stu-id="08175-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="08175-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>упградидитионвиспродукткэймесод</strong></a></span><span class="sxs-lookup"><span data-stu-id="08175-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="08175-137">Активирует устройство для получения ключа продукта и обновления выпуска клиента.</span><span class="sxs-lookup"><span data-stu-id="08175-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="08175-138">Для этого процесса обновления требуется перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="08175-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="08175-139">Поддерживаемая операция — Execute.</span><span class="sxs-lookup"><span data-stu-id="08175-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="08175-140">Когда ключ продукта помещается с сервера MDM на устройство пользователя, <strong>changepk.exe</strong> запускается с помощью ключа продукта.</span><span class="sxs-lookup"><span data-stu-id="08175-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="08175-141">После завершения работы пользователю отображается уведомление о том, что доступен новый выпуск Windows 10.</span><span class="sxs-lookup"><span data-stu-id="08175-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="08175-142">После этого пользователь может перезагрузить систему вручную или, через два часа, устройство будет автоматически перезапущено для завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="08175-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="08175-143">Перед автоматическим перезапуском пользователь получит уведомление за 10 минут.</span><span class="sxs-lookup"><span data-stu-id="08175-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="08175-144">После перезапуска устройства процесс обновления выпуска будет завершен.</span><span class="sxs-lookup"><span data-stu-id="08175-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="08175-145">Пользователь получит уведомление об успешном обновлении.</span><span class="sxs-lookup"><span data-stu-id="08175-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="08175-146">Если другой политике требуется перезагрузка системы, которая происходит при <strong>changepk.exe</strong> выполняется, обновление выпуска завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="08175-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="08175-147">Если ключ продукта вводится в пакете подготовки, и пользователь начинает установку пакета, уведомление отображается пользователю, что для завершения установки пакета будет выполнена перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="08175-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="08175-148">После явного согласия пользователя выполнение пакета продолжается, а <strong>changepk.exe</strong> запускается с помощью ключа продукта.</span><span class="sxs-lookup"><span data-stu-id="08175-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="08175-149">Пользователь получит уведомление с напоминанием за 30 секунд до автоматического перезапуска.</span><span class="sxs-lookup"><span data-stu-id="08175-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="08175-150">После перезапуска устройства процесс обновления выпуска будет завершен.</span><span class="sxs-lookup"><span data-stu-id="08175-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="08175-151">Пользователь получит уведомление об успешном обновлении.</span><span class="sxs-lookup"><span data-stu-id="08175-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="08175-152">Этот узел можно также использовать для активации или изменения ключа продукта в определенном выпуске устройства Windows 10 Desktop, введя ключ продукта.</span><span class="sxs-lookup"><span data-stu-id="08175-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="08175-153">Активация или изменение ключа продукта не требует перезагрузки и является автоматическим процессом для пользователя.</span><span class="sxs-lookup"><span data-stu-id="08175-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="08175-154">Ключ продукта должен состоять из 29 символов (то есть должен включать тире), в противном случае при активации, обновлении выпуска или изменении ключа продукта на устройствах Windows 10 Desktop произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="08175-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="08175-155">Ключ продукта получен из центра поддержки корпоративных лицензий Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="08175-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="08175-156">Чтобы получить доступ к порталу, ваша организация должна иметь контракт корпоративного лицензирования с корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="08175-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="08175-157">Ниже приведены допустимые варианты обновления выпуска при использовании этого узла через MDM:</span><span class="sxs-lookup"><span data-stu-id="08175-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="08175-158">Windows 10 Корпоративная для Windows 10 для образовательных учреждений</span><span class="sxs-lookup"><span data-stu-id="08175-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="08175-159">Windows 10 домашняя для Windows 10 для образовательных учреждений</span><span class="sxs-lookup"><span data-stu-id="08175-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="08175-160">Windows 10 профессиональная для Windows 10 для образовательных учреждений</span><span class="sxs-lookup"><span data-stu-id="08175-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="08175-161">Windows 10 профессиональная для Windows 10 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="08175-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="08175-162">Активация или изменение ключа продукта может быть выполнена в следующих выпусках:</span><span class="sxs-lookup"><span data-stu-id="08175-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="08175-163">Windows 10 для образовательных учреждений</span><span class="sxs-lookup"><span data-stu-id="08175-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="08175-164">Windows 10 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="08175-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="08175-165">Windows 10 Домашняя</span><span class="sxs-lookup"><span data-stu-id="08175-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="08175-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="08175-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="08175-167">Свойства</span><span class="sxs-lookup"><span data-stu-id="08175-167">Properties</span></span>

<span data-ttu-id="08175-168">Класс **MDM \_ виндовслиценсинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="08175-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="08175-169">Выпуск</span><span class="sxs-lookup"><span data-stu-id="08175-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08175-170">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="08175-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08175-171">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="08175-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08175-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08175-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08175-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08175-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08175-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08175-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08175-175">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08175-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08175-176">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="08175-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="08175-177">лиценсекэйтипе</span><span class="sxs-lookup"><span data-stu-id="08175-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08175-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08175-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08175-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="08175-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08175-180">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="08175-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08175-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08175-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08175-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08175-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08175-183">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08175-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08175-184">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="08175-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="08175-185">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="08175-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="08175-186">Состояние</span><span class="sxs-lookup"><span data-stu-id="08175-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08175-187">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="08175-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08175-188">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="08175-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08175-189">Требования</span><span class="sxs-lookup"><span data-stu-id="08175-189">Requirements</span></span>



| <span data-ttu-id="08175-190">Требование</span><span class="sxs-lookup"><span data-stu-id="08175-190">Requirement</span></span> | <span data-ttu-id="08175-191">Значение</span><span class="sxs-lookup"><span data-stu-id="08175-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08175-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08175-192">Minimum supported client</span></span><br/> | <span data-ttu-id="08175-193">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="08175-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08175-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08175-194">Minimum supported server</span></span><br/> | <span data-ttu-id="08175-195">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="08175-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="08175-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="08175-196">Namespace</span></span><br/>                | <span data-ttu-id="08175-197">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="08175-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="08175-198">MOF</span><span class="sxs-lookup"><span data-stu-id="08175-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08175-199"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08175-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="08175-200">DLL</span><span class="sxs-lookup"><span data-stu-id="08175-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08175-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08175-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08175-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08175-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08175-203">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="08175-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

