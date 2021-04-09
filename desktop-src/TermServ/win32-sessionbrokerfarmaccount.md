---
title: Класс Win32_SessionBrokerFarmAccount
description: Класс Win32 \_ сессионброкерфармаккаунт больше не доступен для использования в Windows Server 2012. | Класс Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerFarmAccount службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerFarmAccount, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820821"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="d474c-106">\_Класс Win32 сессионброкерфармаккаунт</span><span class="sxs-lookup"><span data-stu-id="d474c-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="d474c-107">\[Класс **Win32 \_ сессионброкерфармаккаунт** больше не доступен для использования в Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="d474c-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="d474c-108">Определяет учетную запись фермы посредника сеансов.</span><span class="sxs-lookup"><span data-stu-id="d474c-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="d474c-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d474c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d474c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d474c-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="d474c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="d474c-111">Members</span></span>

<span data-ttu-id="d474c-112">Класс **Win32 \_ сессионброкерфармаккаунт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d474c-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="d474c-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d474c-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="d474c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="d474c-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d474c-115">Методы</span><span class="sxs-lookup"><span data-stu-id="d474c-115">Methods</span></span>

<span data-ttu-id="d474c-116">Класс **Win32 \_ сессионброкерфармаккаунт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d474c-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="d474c-117">Метод</span><span class="sxs-lookup"><span data-stu-id="d474c-117">Method</span></span>                                                      | <span data-ttu-id="d474c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d474c-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="d474c-119">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="d474c-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="d474c-120">Удаляет учетную запись фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d474c-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="d474c-121">Properties</span></span>

<span data-ttu-id="d474c-122">Класс **Win32 \_ сессионброкерфармаккаунт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d474c-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d474c-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="d474c-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d474c-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d474c-126">Имя домена, к которому принадлежит учетная запись фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="d474c-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d474c-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d474c-130">Имя учетной записи фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-131">**аккаунтпассворд**</span><span class="sxs-lookup"><span data-stu-id="d474c-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d474c-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d474c-134">Пароль учетной записи фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="d474c-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d474c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d474c-138">Первое имя участника-службы (SPN), связанное с учетной записью фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="d474c-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d474c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d474c-142">Второе имя субъекта-службы, связанное с учетной записью фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-143">**компутерднснаме**</span><span class="sxs-lookup"><span data-stu-id="d474c-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d474c-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d474c-146">DNS-имя компьютера, связанного с учетной записью фермы.</span><span class="sxs-lookup"><span data-stu-id="d474c-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-147">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="d474c-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d474c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d474c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d474c-150">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d474c-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d474c-151">Имя фермы посредника сеансов.</span><span class="sxs-lookup"><span data-stu-id="d474c-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="d474c-152">**Вручную**</span><span class="sxs-lookup"><span data-stu-id="d474c-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474c-153">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d474c-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d474c-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d474c-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d474c-155">Указывает, обновляется ли пароль учетной записи вручную.</span><span class="sxs-lookup"><span data-stu-id="d474c-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d474c-156">Требования</span><span class="sxs-lookup"><span data-stu-id="d474c-156">Requirements</span></span>



| <span data-ttu-id="d474c-157">Требование</span><span class="sxs-lookup"><span data-stu-id="d474c-157">Requirement</span></span> | <span data-ttu-id="d474c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="d474c-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d474c-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d474c-159">Minimum supported client</span></span><br/> | <span data-ttu-id="d474c-160">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d474c-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d474c-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d474c-161">Minimum supported server</span></span><br/> | <span data-ttu-id="d474c-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d474c-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="d474c-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d474c-163">End of client support</span></span><br/>    | <span data-ttu-id="d474c-164">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d474c-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d474c-165">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d474c-165">End of server support</span></span><br/>    | <span data-ttu-id="d474c-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d474c-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="d474c-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d474c-167">Namespace</span></span><br/>                | <span data-ttu-id="d474c-168">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d474c-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d474c-169">MOF</span><span class="sxs-lookup"><span data-stu-id="d474c-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d474c-170"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d474c-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d474c-171">DLL</span><span class="sxs-lookup"><span data-stu-id="d474c-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d474c-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d474c-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

