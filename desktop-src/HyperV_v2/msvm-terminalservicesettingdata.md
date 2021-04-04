---
description: Представляет параметры для служб терминалов виртуальных компьютеров на узле.
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Класс Msvm_TerminalServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811320"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="afa91-103">\_Класс мсвм терминалсервицесеттингдата</span><span class="sxs-lookup"><span data-stu-id="afa91-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="afa91-104">Представляет параметры для служб терминалов виртуальных компьютеров на узле.</span><span class="sxs-lookup"><span data-stu-id="afa91-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="afa91-105">Свойства этого класса нельзя изменить напрямую.</span><span class="sxs-lookup"><span data-stu-id="afa91-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="afa91-106">Клиент должен вызвать метод [**мсвм \_ Терминалсервице. модифисервицесеттингс**](modifyservicesettings-msvm-terminalservice.md) , чтобы изменить любое из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="afa91-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="afa91-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="afa91-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa91-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afa91-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="afa91-109">Члены</span><span class="sxs-lookup"><span data-stu-id="afa91-109">Members</span></span>

<span data-ttu-id="afa91-110">Класс **мсвм \_ терминалсервицесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="afa91-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="afa91-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="afa91-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afa91-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="afa91-112">Properties</span></span>

<span data-ttu-id="afa91-113">Класс **мсвм \_ терминалсервицесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="afa91-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afa91-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="afa91-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-115">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="afa91-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="afa91-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-117">Список хэш-алгоритмов, принятых для проверки подписи федеративных маркеров проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="afa91-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="afa91-118">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="afa91-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="afa91-119">**аусцертификатехаш**</span><span class="sxs-lookup"><span data-stu-id="afa91-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-120">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="afa91-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="afa91-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-122">Хэш сертификата, используемого для удаленной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="afa91-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="afa91-123">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="afa91-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="afa91-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa91-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-126">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="afa91-126">A short description of the object.</span></span> <span data-ttu-id="afa91-127">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afa91-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afa91-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="afa91-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="afa91-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa91-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-131">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="afa91-131">A description of the object.</span></span> <span data-ttu-id="afa91-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afa91-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afa91-133">**дисаблеселфсигнедцертификатеженератион**</span><span class="sxs-lookup"><span data-stu-id="afa91-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="afa91-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afa91-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-136">Отключает Создание самозаверяющего сертификата.</span><span class="sxs-lookup"><span data-stu-id="afa91-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="afa91-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="afa91-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="afa91-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa91-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-140">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="afa91-140">A display name for the object.</span></span> <span data-ttu-id="afa91-141">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afa91-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afa91-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="afa91-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="afa91-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa91-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa91-145">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="afa91-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="afa91-146">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="afa91-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="afa91-147">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afa91-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afa91-148">**листенерпорт**</span><span class="sxs-lookup"><span data-stu-id="afa91-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afa91-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afa91-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-151">Сетевой порт, на котором будет установлено первоначальное подключение к удаленному сеансу.</span><span class="sxs-lookup"><span data-stu-id="afa91-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="afa91-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="afa91-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa91-153">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="afa91-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="afa91-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afa91-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa91-155">Список хэшей сертификатов доверенных издателей для проверки подписи федеративных маркеров проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="afa91-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="afa91-156">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="afa91-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afa91-157">Требования</span><span class="sxs-lookup"><span data-stu-id="afa91-157">Requirements</span></span>



| <span data-ttu-id="afa91-158">Требование</span><span class="sxs-lookup"><span data-stu-id="afa91-158">Requirement</span></span> | <span data-ttu-id="afa91-159">Значение</span><span class="sxs-lookup"><span data-stu-id="afa91-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa91-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afa91-160">Minimum supported client</span></span><br/> | <span data-ttu-id="afa91-161">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="afa91-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="afa91-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afa91-162">Minimum supported server</span></span><br/> | <span data-ttu-id="afa91-163">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="afa91-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="afa91-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="afa91-164">Namespace</span></span><br/>                | <span data-ttu-id="afa91-165">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="afa91-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="afa91-166">MOF</span><span class="sxs-lookup"><span data-stu-id="afa91-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afa91-167"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afa91-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="afa91-168">DLL</span><span class="sxs-lookup"><span data-stu-id="afa91-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afa91-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="afa91-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

