---
description: '&Win32 \_ нетворклогинпрофиле \# 8194; Класс WMI представляет данные сетевого входа конкретного пользователя в компьютерной системе под Windows.'
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Класс Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650454"
---
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="289f4-103">\_Класс Win32 нетворклогинпрофиле</span><span class="sxs-lookup"><span data-stu-id="289f4-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="289f4-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ нетворклогинпрофиле для Win32** представляет данные сетевого входа конкретного пользователя в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="289f4-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="289f4-105">Сюда входят, но не ограничиваются состояние пароля, права доступа, дисковые квоты и пути к каталогам входа.</span><span class="sxs-lookup"><span data-stu-id="289f4-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="289f4-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="289f4-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="289f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="289f4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a><span data-ttu-id="289f4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="289f4-108">Members</span></span>

<span data-ttu-id="289f4-109">Класс **Win32 \_ нетворклогинпрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="289f4-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="289f4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="289f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="289f4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="289f4-111">Properties</span></span>

<span data-ttu-id="289f4-112">Класс **Win32 \_ нетворклогинпрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="289f4-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="289f4-113">**AccountExpires**</span><span class="sxs-lookup"><span data-stu-id="289f4-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-114">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="289f4-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-116">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ acct \_ Expires")</span><span class="sxs-lookup"><span data-stu-id="289f4-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-117">Срок действия учетной записи истечет.</span><span class="sxs-lookup"><span data-stu-id="289f4-117">Account will expire.</span></span> <span data-ttu-id="289f4-118">Это значение вычисляется на основе числа секунд, истекших с 00:00:00 1 января 1970, и задается в следующем формате: YYYYMMDDHHMMSS. мммммм сутк.</span><span class="sxs-lookup"><span data-stu-id="289f4-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="289f4-119">Пример: 20521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="289f4-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="289f4-120">**аусоризатионфлагс**</span><span class="sxs-lookup"><span data-stu-id="289f4-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-121">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-123">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags проверки подлинности \_ "), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("принтер", "связь", "сервер", "учетные записи")</span><span class="sxs-lookup"><span data-stu-id="289f4-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-124">Набор флагов, указывающих ресурсы, которые пользователь имеет право использовать или изменять.</span><span class="sxs-lookup"><span data-stu-id="289f4-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="289f4-125">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="289f4-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-126">Принтер</span><span class="sxs-lookup"><span data-stu-id="289f4-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="289f4-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="289f4-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-128">Связь</span><span class="sxs-lookup"><span data-stu-id="289f4-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="289f4-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="289f4-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-130">Сервер</span><span class="sxs-lookup"><span data-stu-id="289f4-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="289f4-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="289f4-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-132">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="289f4-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="289f4-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="289f4-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-136">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management functions \| нетусеренум")</span><span class="sxs-lookup"><span data-stu-id="289f4-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-137">Количество неудачных попыток ввода пароля при входе в систему компьютера под Windows.</span><span class="sxs-lookup"><span data-stu-id="289f4-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="289f4-138">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="289f4-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="289f4-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="289f4-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-142">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="289f4-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="289f4-143">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="289f4-143">Short textual description of the current object.</span></span>

<span data-ttu-id="289f4-144">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="289f4-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="289f4-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-148">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ кодовая \_ Страница")</span><span class="sxs-lookup"><span data-stu-id="289f4-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-149">Кодовая страница для выбранного языка пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="289f4-150">Кодовая страница — это используемая кодировка.</span><span class="sxs-lookup"><span data-stu-id="289f4-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-151">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="289f4-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-154">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")</span><span class="sxs-lookup"><span data-stu-id="289f4-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-155">Комментарий или описание для этого профиля входа.</span><span class="sxs-lookup"><span data-stu-id="289f4-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-156">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="289f4-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-159">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ код страны")</span><span class="sxs-lookup"><span data-stu-id="289f4-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-160">Код страны или региона для выбранного языка пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-161">**Описание**</span><span class="sxs-lookup"><span data-stu-id="289f4-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="289f4-164">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="289f4-164">Textual description of the current object.</span></span>

<span data-ttu-id="289f4-165">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="289f4-166">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="289f4-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-169">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("сценарий", "учетная запись отключена", "Корневая папка обязательна", "Блокировка", "пароль не требуется", "пасвворд не может изменить", "разрешен зашифрованный тестовый пароль", "временная повторяющаяся учетная запись", "Обычная учетная записи", "учетная запись междоменного доверия", "учетная запись доверия рабочей станции", "учетная запись доверия сервера", "не срок действия пароля", "учетная запись MNS", "требуемая смарт-карта", "доверенный для делегирования", "не делегировано", "использовать только ключ DES", "не требовать предварительной проверки", "срок действия пароля истек")</span><span class="sxs-lookup"><span data-stu-id="289f4-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-170">Свойства, доступные для этого сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="289f4-170">The properties available to this network profile.</span></span>

<span data-ttu-id="289f4-171">К свойствам, которые можно задать, относятся:</span><span class="sxs-lookup"><span data-stu-id="289f4-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="289f4-172">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="289f4-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-173">Скрипт</span><span class="sxs-lookup"><span data-stu-id="289f4-173">Script</span></span>

<span data-ttu-id="289f4-174">Выполнен сценарий входа.</span><span class="sxs-lookup"><span data-stu-id="289f4-174">A logon script executed.</span></span> <span data-ttu-id="289f4-175">Это значение должно быть установлено для LAN Manager 2,0.</span><span class="sxs-lookup"><span data-stu-id="289f4-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-176">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="289f4-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-177">Учетная запись отключена</span><span class="sxs-lookup"><span data-stu-id="289f4-177">Account Disabled</span></span>

<span data-ttu-id="289f4-178">Учетная запись пользователя отключена.</span><span class="sxs-lookup"><span data-stu-id="289f4-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-179">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="289f4-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-180">Требуется домашний каталог</span><span class="sxs-lookup"><span data-stu-id="289f4-180">Home Directory Required</span></span>

<span data-ttu-id="289f4-181">Требуется домашний каталог.</span><span class="sxs-lookup"><span data-stu-id="289f4-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-182">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="289f4-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-183">Блокирование</span><span class="sxs-lookup"><span data-stu-id="289f4-183">Lockout</span></span>

<span data-ttu-id="289f4-184">Учетная запись в данный момент заблокирована. Для [**нетусерсетинфо**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)это значение можно снять, чтобы разблокировать ранее заблокированную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="289f4-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="289f4-185">Это значение нельзя использовать для блокировки ранее незаблокированной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="289f4-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-186">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="289f4-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-187">Пароль не требуется</span><span class="sxs-lookup"><span data-stu-id="289f4-187">Password Not Required</span></span>

<span data-ttu-id="289f4-188">Пароль не требуется.</span><span class="sxs-lookup"><span data-stu-id="289f4-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-189">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="289f4-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-190">Пароль не может быть изменен</span><span class="sxs-lookup"><span data-stu-id="289f4-190">Password Cannot Change</span></span>

<span data-ttu-id="289f4-191">Пользователь не может изменить пароль.</span><span class="sxs-lookup"><span data-stu-id="289f4-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-192">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="289f4-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-193">Зашифрованный тестовый пароль разрешен</span><span class="sxs-lookup"><span data-stu-id="289f4-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="289f4-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="289f4-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-195">Временная повторяющаяся учетная запись</span><span class="sxs-lookup"><span data-stu-id="289f4-195">Temp Duplicate Account</span></span>

<span data-ttu-id="289f4-196">Учетная запись для пользователей, Главная учетная запись которых находится в другом домене.</span><span class="sxs-lookup"><span data-stu-id="289f4-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="289f4-197">Эта учетная запись предоставляет пользователю доступ к этому домену, но не к домену, который доверяет данному домену.</span><span class="sxs-lookup"><span data-stu-id="289f4-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="289f4-198">Диспетчер пользователей ссылается на этот тип учетной записи в качестве учетной записи локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-199">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="289f4-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-200">Обычная учетная запись</span><span class="sxs-lookup"><span data-stu-id="289f4-200">Normal Account</span></span>

<span data-ttu-id="289f4-201">Тип учетной записи по умолчанию, представляющий обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-202">2048 (0x800)</span><span class="sxs-lookup"><span data-stu-id="289f4-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-203">Учетная запись междоменного доверия</span><span class="sxs-lookup"><span data-stu-id="289f4-203">Interdomain Trust Account</span></span>

<span data-ttu-id="289f4-204">Разрешение на учетную запись доверия для домена, который доверяет другим доменам.</span><span class="sxs-lookup"><span data-stu-id="289f4-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-205">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="289f4-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-206">Учетная запись доверия рабочей станции</span><span class="sxs-lookup"><span data-stu-id="289f4-206">Workstation Trust Account</span></span>

<span data-ttu-id="289f4-207">Учетная запись компьютера для рабочей станции или сервера Windows, который является членом этого домена.</span><span class="sxs-lookup"><span data-stu-id="289f4-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-208">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="289f4-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-209">Учетная запись доверия сервера</span><span class="sxs-lookup"><span data-stu-id="289f4-209">Server Trust Account</span></span>

<span data-ttu-id="289f4-210">Учетная запись компьютера для резервного контроллера домена, который является членом этого домена.</span><span class="sxs-lookup"><span data-stu-id="289f4-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-211">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="289f4-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-212">Срок действия пароля не истек</span><span class="sxs-lookup"><span data-stu-id="289f4-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="289f4-213">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="289f4-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-214">Учетная запись MNS</span><span class="sxs-lookup"><span data-stu-id="289f4-214">MNS Logon Account</span></span>

<span data-ttu-id="289f4-215">Тип учетной записи входа в набор узлов большинства (MNS), представляющий пользователя MNS.</span><span class="sxs-lookup"><span data-stu-id="289f4-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-216">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="289f4-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-217">Требуется смарт-карта</span><span class="sxs-lookup"><span data-stu-id="289f4-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="289f4-218">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="289f4-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-219">Доверенный для делегирования</span><span class="sxs-lookup"><span data-stu-id="289f4-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="289f4-220">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="289f4-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-221">Не делегировано</span><span class="sxs-lookup"><span data-stu-id="289f4-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="289f4-222">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="289f4-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-223">Использовать только ключ DES</span><span class="sxs-lookup"><span data-stu-id="289f4-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="289f4-224">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="289f4-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-225">Не требовать предварительной разработки</span><span class="sxs-lookup"><span data-stu-id="289f4-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="289f4-226">8388608 (0x800000)</span><span class="sxs-lookup"><span data-stu-id="289f4-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="289f4-227">Срок действия пароля истек</span><span class="sxs-lookup"><span data-stu-id="289f4-227">Password Expired</span></span>

<span data-ttu-id="289f4-228">Указывает, что срок действия пароля истек.</span><span class="sxs-lookup"><span data-stu-id="289f4-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="289f4-229">Следующие свойства описывают тип учетной записи.</span><span class="sxs-lookup"><span data-stu-id="289f4-229">The following properties describe the account type.</span></span> <span data-ttu-id="289f4-230">Можно задать только одно значение:</span><span class="sxs-lookup"><span data-stu-id="289f4-230">Only one value can be set:</span></span>

-   <span data-ttu-id="289f4-231">\_Обычная \_ учетная запись УФ</span><span class="sxs-lookup"><span data-stu-id="289f4-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="289f4-232">УФ \_ временная \_ \_ учетная запись повторения</span><span class="sxs-lookup"><span data-stu-id="289f4-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="289f4-233">\_ \_ учетная запись доверия рабочей станции УФ \_</span><span class="sxs-lookup"><span data-stu-id="289f4-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="289f4-234">\_ \_ \_ учетная запись доверия сервера УФ</span><span class="sxs-lookup"><span data-stu-id="289f4-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="289f4-235">\_ \_ учетная запись междоменного доверия УФ \_</span><span class="sxs-lookup"><span data-stu-id="289f4-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="289f4-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="289f4-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-239">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ полное \_ имя")</span><span class="sxs-lookup"><span data-stu-id="289f4-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-240">Полное имя пользователя, принадлежащего профилю сетевого входа.</span><span class="sxs-lookup"><span data-stu-id="289f4-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="289f4-241">Эта строка может быть пустой, если пользователь решает не связывать полное имя с именем пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="289f4-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-245">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ корневая \_ Папка")</span><span class="sxs-lookup"><span data-stu-id="289f4-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-246">Путь к домашнему каталогу пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-246">Path to the home directory of the user.</span></span> <span data-ttu-id="289f4-247">Эта строка может быть пустой, если пользователь решил не указывать домашний каталог.</span><span class="sxs-lookup"><span data-stu-id="289f4-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="289f4-248">Пример: " \\ хомедир"</span><span class="sxs-lookup"><span data-stu-id="289f4-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="289f4-249">**хомедиректоридриве**</span><span class="sxs-lookup"><span data-stu-id="289f4-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-252">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")</span><span class="sxs-lookup"><span data-stu-id="289f4-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-253">Буква диска, назначенная домашнему каталогу пользователя для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="289f4-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="289f4-254">Пример: "C:"</span><span class="sxs-lookup"><span data-stu-id="289f4-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="289f4-255">**ластлогофф**</span><span class="sxs-lookup"><span data-stu-id="289f4-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-256">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="289f4-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-258">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ последний \_ Выход ")</span><span class="sxs-lookup"><span data-stu-id="289f4-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-259">Последнее выход пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="289f4-259">User last logged off the system.</span></span> <span data-ttu-id="289f4-260">Это значение вычисляется на основе числа секунд, прошедших с 00:00:00 1 января 1970 г.</span><span class="sxs-lookup"><span data-stu-id="289f4-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="289f4-261">Значение " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " означает, что время последнего выхода из системы неизвестно.</span><span class="sxs-lookup"><span data-stu-id="289f4-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="289f4-262">Это значение имеет формат YYYYMMDDHHMMSS. мммммм сутк.</span><span class="sxs-lookup"><span data-stu-id="289f4-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="289f4-263">Сведения о переводе этого свойства в местное время см. в разделе [задачи WMI: даты и время](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="289f4-264">Пример: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="289f4-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="289f4-265">**ластлогон**</span><span class="sxs-lookup"><span data-stu-id="289f4-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-266">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="289f4-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-268">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ прошлый \_ Вход")</span><span class="sxs-lookup"><span data-stu-id="289f4-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-269">Последний пользователь вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="289f4-269">User last logged on to the system.</span></span> <span data-ttu-id="289f4-270">Это значение вычисляется на основе числа секунд, прошедших с 00:00:00 1 января 1970 г.</span><span class="sxs-lookup"><span data-stu-id="289f4-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="289f4-271">Это значение имеет формат YYYYMMDDHHMMSS. мммммм сутк.</span><span class="sxs-lookup"><span data-stu-id="289f4-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="289f4-272">Сведения о переводе этого свойства в местное время см. в разделе [задачи WMI: даты и время](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="289f4-273">Пример: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="289f4-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="289f4-274">**логонхаурс**</span><span class="sxs-lookup"><span data-stu-id="289f4-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-277">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ hours")</span><span class="sxs-lookup"><span data-stu-id="289f4-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-278">Раз в неделю, когда пользователь может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="289f4-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="289f4-279">Каждый бит представляет единицу времени, заданную свойством **унитспервик** .</span><span class="sxs-lookup"><span data-stu-id="289f4-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="289f4-280">Например, если единицей времени является час, первый бит (бит 0, слово 0) — воскресенье, 0:00 – 0:59, второй бит (бит 1, слово 0) — воскресенье, 1:00 — 1:59 и т. д.</span><span class="sxs-lookup"><span data-stu-id="289f4-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="289f4-281">Если этому члену присвоено **значение NULL**, ограничение времени отсутствует.</span><span class="sxs-lookup"><span data-stu-id="289f4-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="289f4-282">Время устанавливается в формате GMT и должно быть скорректировано для других часовых поясов (например, GMT минус 8 часов для PST).</span><span class="sxs-lookup"><span data-stu-id="289f4-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="289f4-283">**логонсервер**</span><span class="sxs-lookup"><span data-stu-id="289f4-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-286">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ Server")</span><span class="sxs-lookup"><span data-stu-id="289f4-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-287">Имя сервера, на который отправляются запросы на вход.</span><span class="sxs-lookup"><span data-stu-id="289f4-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="289f4-288">Именам серверов должны предшествовать две обратные косые черты ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="289f4-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="289f4-289">Имя сервера со звездочкой ( \\ \\ \* ) указывает на то, что запрос на вход может обрабатываться любым сервером входа.</span><span class="sxs-lookup"><span data-stu-id="289f4-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="289f4-290">Строка NULL указывает, что запросы отправляются на контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="289f4-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="289f4-291">Пример: " \\ \\ MyServer"</span><span class="sxs-lookup"><span data-stu-id="289f4-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="289f4-292">**максимумстораже**</span><span class="sxs-lookup"><span data-stu-id="289f4-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-293">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="289f4-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-295">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="289f4-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-296">Максимальный объем свободного места на диске, доступный пользователю.</span><span class="sxs-lookup"><span data-stu-id="289f4-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="289f4-297">Если Максимумстораже имеет значение USER \_ максстораже \_ ununlimited, то пользователю будет разрешено использовать все доступное место на диске.</span><span class="sxs-lookup"><span data-stu-id="289f4-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="289f4-298">Пример: 10000000</span><span class="sxs-lookup"><span data-stu-id="289f4-298">Example: 10000000</span></span>

<span data-ttu-id="289f4-299">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="289f4-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="289f4-300">**Name**</span><span class="sxs-lookup"><span data-stu-id="289f4-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-303">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сетевое управление структуры управления \| [**\_ сведениями о пользователях \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ имя")</span><span class="sxs-lookup"><span data-stu-id="289f4-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-304">Учетная запись пользователя в определенном домене или компьютере.</span><span class="sxs-lookup"><span data-stu-id="289f4-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="289f4-305">Число символов в имени не может превышать значение УНЛЕН.</span><span class="sxs-lookup"><span data-stu-id="289f4-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="289f4-306">Пример: "somedomain \\ JohnDoe"</span><span class="sxs-lookup"><span data-stu-id="289f4-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="289f4-307">**нумберофлогонс**</span><span class="sxs-lookup"><span data-stu-id="289f4-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-308">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-310">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ NUM \_ logon")</span><span class="sxs-lookup"><span data-stu-id="289f4-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-311">Количество успешных попыток входа пользователя в эту учетную запись.</span><span class="sxs-lookup"><span data-stu-id="289f4-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="289f4-312">Значение 0xFFFFFFFF указывает, что значение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="289f4-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="289f4-313">Это свойство хранится отдельно на каждом резервном контроллере домена (BDC) в домене.</span><span class="sxs-lookup"><span data-stu-id="289f4-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="289f4-314">Чтобы получить точное значение, следует использовать только самое большое значение из всех BDC.</span><span class="sxs-lookup"><span data-stu-id="289f4-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="289f4-315">Пример: 4</span><span class="sxs-lookup"><span data-stu-id="289f4-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="289f4-316">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="289f4-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-319">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ пармс")</span><span class="sxs-lookup"><span data-stu-id="289f4-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-320">Пространство, заданное для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="289f4-320">Space set aside for use by applications.</span></span> <span data-ttu-id="289f4-321">Эта строка может иметь значение null или содержать любое число символов перед завершающим нулевым символом.</span><span class="sxs-lookup"><span data-stu-id="289f4-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="289f4-322">Продукты Майкрософт используют этот элемент для хранения сведений о конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="289f4-323">Не изменяйте эти сведения, так как это значение характерно для приложения.</span><span class="sxs-lookup"><span data-stu-id="289f4-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-324">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="289f4-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-325">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="289f4-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-327">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ пароль \_ ")</span><span class="sxs-lookup"><span data-stu-id="289f4-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-328">Срок действия пароля.</span><span class="sxs-lookup"><span data-stu-id="289f4-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="289f4-329">Это значение измеряется из числа секунд, прошедшего с момента последнего изменения пароля.</span><span class="sxs-lookup"><span data-stu-id="289f4-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="289f4-330">Пример: 00001201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="289f4-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="289f4-331">**пассвордекспирес**</span><span class="sxs-lookup"><span data-stu-id="289f4-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-332">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="289f4-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-334">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**пользовательские \_ модальные \_ данные \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ Age ")</span><span class="sxs-lookup"><span data-stu-id="289f4-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-335">Дата и время истечения срока действия пароля.</span><span class="sxs-lookup"><span data-stu-id="289f4-335">Date and time the password expires.</span></span> <span data-ttu-id="289f4-336">Значение задается в следующем формате: YYYYMMDDHHMMSS. мммммм сутк</span><span class="sxs-lookup"><span data-stu-id="289f4-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="289f4-337">Пример: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="289f4-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="289f4-338">**примариграупид**</span><span class="sxs-lookup"><span data-stu-id="289f4-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-339">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-341">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ идентификатор основной группы \_ ")</span><span class="sxs-lookup"><span data-stu-id="289f4-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-342">Относительный идентификатор (RID) основной глобальной группы для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="289f4-343">Идентификатор проверяет основную группу, к которой принадлежит профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-344">**Права**</span><span class="sxs-lookup"><span data-stu-id="289f4-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-345">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-347">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Priv")</span><span class="sxs-lookup"><span data-stu-id="289f4-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-348">Уровень привилегий, назначенный свойству **usri3 \_ Name** .</span><span class="sxs-lookup"><span data-stu-id="289f4-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="289f4-349">**Гость** (0)</span><span class="sxs-lookup"><span data-stu-id="289f4-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="289f4-350">**Пользователь** (1)</span><span class="sxs-lookup"><span data-stu-id="289f4-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="289f4-351">**Администратор** (2)</span><span class="sxs-lookup"><span data-stu-id="289f4-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="289f4-352">**Профиль**</span><span class="sxs-lookup"><span data-stu-id="289f4-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-355">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Profile")</span><span class="sxs-lookup"><span data-stu-id="289f4-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-356">Путь к профилю пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-356">Path to the user's profile.</span></span> <span data-ttu-id="289f4-357">Это значение может быть пустой строкой, локальным абсолютным путем или UNC-путем.</span><span class="sxs-lookup"><span data-stu-id="289f4-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="289f4-358">Профиль пользователя содержит параметры, настраиваемые для каждого пользователя, например цвета рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="289f4-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="289f4-359">Пример: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="289f4-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="289f4-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="289f4-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-363">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ путь к скрипту usri3 \_ ")</span><span class="sxs-lookup"><span data-stu-id="289f4-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-364">Путь к каталогу для сценария входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="289f4-365">Сценарий входа автоматически выполняет набор команд при каждом входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="289f4-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="289f4-366">Пример: "C: \\ Win \\ Profiles \\ сомасстевен"</span><span class="sxs-lookup"><span data-stu-id="289f4-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="289f4-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="289f4-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-368">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-370">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="289f4-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="289f4-371">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="289f4-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="289f4-372">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="289f4-373">**унитспервик**</span><span class="sxs-lookup"><span data-stu-id="289f4-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-374">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-376">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ единицы \_ в \_ неделю")</span><span class="sxs-lookup"><span data-stu-id="289f4-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-377">Количество единиц времени, на которое делится неделя.</span><span class="sxs-lookup"><span data-stu-id="289f4-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="289f4-378">Он используется со свойством **логонхаурс** для ограничения доступа пользователя к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="289f4-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="289f4-379">Пример: 168 (ч в неделю)</span><span class="sxs-lookup"><span data-stu-id="289f4-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="289f4-380">**усеркоммент**</span><span class="sxs-lookup"><span data-stu-id="289f4-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-383">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**пользователя \_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment ")</span><span class="sxs-lookup"><span data-stu-id="289f4-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-384">Определенный пользователем комментарий или описание для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="289f4-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-385">**UserId**</span><span class="sxs-lookup"><span data-stu-id="289f4-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-386">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="289f4-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-388">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ ID пользователя")</span><span class="sxs-lookup"><span data-stu-id="289f4-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-389">RID пользователя.</span><span class="sxs-lookup"><span data-stu-id="289f4-389">RID of the user.</span></span> <span data-ttu-id="289f4-390">Идентификатор проверяет, существует ли пользователь и уникален для этого домена.</span><span class="sxs-lookup"><span data-stu-id="289f4-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="289f4-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="289f4-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-392">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-394">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags")</span><span class="sxs-lookup"><span data-stu-id="289f4-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-395">Тип учетной записи, к которой у пользователя есть права.</span><span class="sxs-lookup"><span data-stu-id="289f4-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="289f4-396">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="289f4-396">The values are:</span></span>

-   <span data-ttu-id="289f4-397">"Обычная учетная запись"</span><span class="sxs-lookup"><span data-stu-id="289f4-397">"Normal Account"</span></span>
-   <span data-ttu-id="289f4-398">"Дублировать учетную запись"</span><span class="sxs-lookup"><span data-stu-id="289f4-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="289f4-399">"Учетная запись доверия рабочей станции"</span><span class="sxs-lookup"><span data-stu-id="289f4-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="289f4-400">"Учетная запись доверия сервера"</span><span class="sxs-lookup"><span data-stu-id="289f4-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="289f4-401">"Учетная запись междоменного доверия"</span><span class="sxs-lookup"><span data-stu-id="289f4-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="289f4-402">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="289f4-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="289f4-403">**Обычная учетная запись** ("Обычная учетная запись")</span><span class="sxs-lookup"><span data-stu-id="289f4-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="289f4-404">**Повторяющаяся учетная запись** ("повторяющаяся учетная запись")</span><span class="sxs-lookup"><span data-stu-id="289f4-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="289f4-405">**Учетная запись доверия рабочей станции** ("учетная запись доверия рабочей станции")</span><span class="sxs-lookup"><span data-stu-id="289f4-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="289f4-406">**Учетная запись доверия сервера** ("учетная запись доверия сервера")</span><span class="sxs-lookup"><span data-stu-id="289f4-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="289f4-407">**Учетная запись междоменного доверия** ("учетная запись междоменного доверия")</span><span class="sxs-lookup"><span data-stu-id="289f4-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="289f4-408">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="289f4-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="289f4-409">**Рабочих станций**</span><span class="sxs-lookup"><span data-stu-id="289f4-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289f4-410">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="289f4-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="289f4-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289f4-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="289f4-412">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры управления сетями \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Workstations")</span><span class="sxs-lookup"><span data-stu-id="289f4-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="289f4-413">Имена рабочих станций, с которых пользователь может выполнять вход.</span><span class="sxs-lookup"><span data-stu-id="289f4-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="289f4-414">Можно указать до восьми рабочих станций. имена должны быть разделены запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="289f4-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="289f4-415">Пустая строка указывает на отсутствие ограничений.</span><span class="sxs-lookup"><span data-stu-id="289f4-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="289f4-416">Чтобы отключить вход от всех рабочих станций к этой учетной записи, задайте \_ АККАУНТДИСАБЛЕ УФ в свойстве **flags** этого класса.</span><span class="sxs-lookup"><span data-stu-id="289f4-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="289f4-417">Комментарии</span><span class="sxs-lookup"><span data-stu-id="289f4-417">Remarks</span></span>

<span data-ttu-id="289f4-418">Класс **Win32 \_ нетворклогинпрофиле** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="289f4-419">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="289f4-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="289f4-420">Дополнительные сведения см. в разделе [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="289f4-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="289f4-421">Примеры</span><span class="sxs-lookup"><span data-stu-id="289f4-421">Examples</span></span>

<span data-ttu-id="289f4-422">Пример " [список профилей входа в сеть](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) " PowerShell возвращает данные сетевого входа для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="289f4-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="289f4-423">Следующий пример на языке VBScript возвращает данные сетевого входа.</span><span class="sxs-lookup"><span data-stu-id="289f4-423">The following VBScript sample returns network login information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a><span data-ttu-id="289f4-424">Требования</span><span class="sxs-lookup"><span data-stu-id="289f4-424">Requirements</span></span>



| <span data-ttu-id="289f4-425">Требование</span><span class="sxs-lookup"><span data-stu-id="289f4-425">Requirement</span></span> | <span data-ttu-id="289f4-426">Значение</span><span class="sxs-lookup"><span data-stu-id="289f4-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="289f4-427">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="289f4-427">Minimum supported client</span></span><br/> | <span data-ttu-id="289f4-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="289f4-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="289f4-429">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="289f4-429">Minimum supported server</span></span><br/> | <span data-ttu-id="289f4-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="289f4-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="289f4-431">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="289f4-431">Namespace</span></span><br/>                | <span data-ttu-id="289f4-432">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="289f4-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="289f4-433">MOF</span><span class="sxs-lookup"><span data-stu-id="289f4-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="289f4-434"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="289f4-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="289f4-435">DLL</span><span class="sxs-lookup"><span data-stu-id="289f4-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="289f4-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="289f4-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="289f4-437">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="289f4-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289f4-438">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="289f4-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="289f4-439">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="289f4-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
