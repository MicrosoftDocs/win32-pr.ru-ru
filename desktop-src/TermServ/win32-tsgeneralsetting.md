---
title: Класс Win32_TSGeneralSetting
description: Представляет общие параметры терминала, такие как уровень шифрования и транспортный протокол.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGeneralSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGeneralSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802482"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="645b6-105">\_Класс Win32 тсженералсеттинг</span><span class="sxs-lookup"><span data-stu-id="645b6-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="645b6-106">Класс **WMI \_ Тсженералсеттинг для Win32** представляет общие параметры терминала, такие как уровень шифрования и транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="645b6-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="645b6-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="645b6-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="645b6-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="645b6-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="645b6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="645b6-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="645b6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="645b6-110">Members</span></span>

<span data-ttu-id="645b6-111">Класс **Win32 \_ тсженералсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="645b6-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="645b6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="645b6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="645b6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="645b6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="645b6-114">Методы</span><span class="sxs-lookup"><span data-stu-id="645b6-114">Methods</span></span>

<span data-ttu-id="645b6-115">Класс **Win32 \_ тсженералсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="645b6-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="645b6-116">Метод</span><span class="sxs-lookup"><span data-stu-id="645b6-116">Method</span></span>                                                                                        | <span data-ttu-id="645b6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="645b6-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="645b6-118">**сетенкриптионлевел**</span><span class="sxs-lookup"><span data-stu-id="645b6-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="645b6-119">Задает уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="645b6-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="645b6-120">**сетсекуритилайер**</span><span class="sxs-lookup"><span data-stu-id="645b6-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="645b6-121">Устанавливает для уровня безопасности один из параметров: "уровень безопасности RDP" (0), "Negotiate" (1) или "SSL" (2).</span><span class="sxs-lookup"><span data-stu-id="645b6-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="645b6-122">**сетусераусентикатионрекуиред**</span><span class="sxs-lookup"><span data-stu-id="645b6-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="645b6-123">Включает или отключает требование, которое пользователи должны пройти проверку подлинности во время соединения, задав значение свойства **усераусентикатионрекуиред** .</span><span class="sxs-lookup"><span data-stu-id="645b6-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="645b6-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="645b6-124">Properties</span></span>

<span data-ttu-id="645b6-125">Класс **Win32 \_ тсженералсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="645b6-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="645b6-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="645b6-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645b6-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="645b6-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="645b6-130">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="645b6-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="645b6-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="645b6-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="645b6-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="645b6-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-135">Отображаемое имя для имени субъекта личного сертификата локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="645b6-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="645b6-136">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="645b6-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-137">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="645b6-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="645b6-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-139">Содержит сериализованное хранилище сертификатов, содержащее все сертификаты из хранилища **учетных записей пользователей** на компьютере, которые являются действительными сертификатами сервера для использования с протоколом SSL.</span><span class="sxs-lookup"><span data-stu-id="645b6-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="645b6-140">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="645b6-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="645b6-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="645b6-143">Описательное имя сочетания уровня сеанса и транспортного протокола.</span><span class="sxs-lookup"><span data-stu-id="645b6-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="645b6-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="645b6-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-147">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="645b6-147">Description of the object.</span></span>

<span data-ttu-id="645b6-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="645b6-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="645b6-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="645b6-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-150">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="645b6-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645b6-152">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="645b6-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="645b6-153">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="645b6-153">The date the object was installed.</span></span> <span data-ttu-id="645b6-154">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="645b6-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="645b6-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="645b6-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="645b6-156">**миненкриптионлевел**</span><span class="sxs-lookup"><span data-stu-id="645b6-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645b6-159">Квалификаторы: **низкий** ("только данные, отправленные с клиента на сервер, защищаются с помощью шифрования на основе силы стандартного ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="645b6-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="645b6-160">Данные, отправляемые с сервера на клиент, не защищены. "), **Medium** (" все данные, передаваемые между сервером и клиентом, защищаются с помощью шифрования на основе стандартной силы ключа сервера ")," **высокий** "(" все данные, передаваемые между сервером и клиентом "защищены с помощью максимальной силы ключа сервера на основе шифрования").</span><span class="sxs-lookup"><span data-stu-id="645b6-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="645b6-161">Минимальный уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="645b6-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="645b6-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкая** (1)</span><span class="sxs-lookup"><span data-stu-id="645b6-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-163">Низкий уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="645b6-163">Low level of encryption.</span></span> <span data-ttu-id="645b6-164">С помощью 56-разрядного шифрования шифруются только данные, отправленные с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="645b6-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="645b6-165">Учтите, что данные, отправляемые с сервера клиенту, не шифруются.</span><span class="sxs-lookup"><span data-stu-id="645b6-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="645b6-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Средний/совместимый с клиентом** (2)</span><span class="sxs-lookup"><span data-stu-id="645b6-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-167">Совместимый с клиентом уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="645b6-167">Client compatible level of encryption.</span></span> <span data-ttu-id="645b6-168">Все данные, отправляемые от клиента серверу и от сервера к клиенту, шифруются по максимальному ключу, поддерживаемому клиентом.</span><span class="sxs-lookup"><span data-stu-id="645b6-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="645b6-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Высокий** (3)</span><span class="sxs-lookup"><span data-stu-id="645b6-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-170">Высокий уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="645b6-170">High level of encryption.</span></span> <span data-ttu-id="645b6-171">Все данные, отправленные с клиента на сервер и с сервера на клиент, шифруются с помощью надежного 128-разрядного шифрования.</span><span class="sxs-lookup"><span data-stu-id="645b6-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="645b6-172">Клиенты, не поддерживающие этот уровень шифрования, не могут подключиться.</span><span class="sxs-lookup"><span data-stu-id="645b6-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="645b6-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS-совместимый** (4)</span><span class="sxs-lookup"><span data-stu-id="645b6-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-174">Шифрование, совместимое с FIPS.</span><span class="sxs-lookup"><span data-stu-id="645b6-174">FIPS compliant encryption.</span></span> <span data-ttu-id="645b6-175">Все данные, отправляемые от клиента серверу и от сервера к клиенту, шифруются и расшифровываются с помощью алгоритмов шифрования FIPS, использующих криптографические модули (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="645b6-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="645b6-176">FIPS — это стандартное право «требования безопасности для криптографических модулей».</span><span class="sxs-lookup"><span data-stu-id="645b6-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="645b6-177">FIPS 140-1 (1994) и FIPS 140-2 (2001) описывают требования правительства для аппаратных и программных криптографических модулей, используемых в правительственных учреждениях США.</span><span class="sxs-lookup"><span data-stu-id="645b6-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="645b6-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-181">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="645b6-181">The name of the object.</span></span>

<span data-ttu-id="645b6-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="645b6-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="645b6-183">**полицисаурцеминенкриптионлевел**</span><span class="sxs-lookup"><span data-stu-id="645b6-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-184">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-186">Указывает, настроено ли свойство **миненкриптионлевел** сервером по групповой политике или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="645b6-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="645b6-187">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="645b6-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-188">Сервер</span><span class="sxs-lookup"><span data-stu-id="645b6-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="645b6-189">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="645b6-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-190">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="645b6-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="645b6-191">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="645b6-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-192">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="645b6-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-193">**полицисаурцесекуритилайер**</span><span class="sxs-lookup"><span data-stu-id="645b6-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-194">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-196">Указывает, настроено ли свойство **секуритилайер** сервером по групповой политике или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="645b6-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="645b6-197">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="645b6-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-198">Сервер</span><span class="sxs-lookup"><span data-stu-id="645b6-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="645b6-199">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="645b6-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-200">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="645b6-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="645b6-201">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="645b6-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-202">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="645b6-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-203">**полицисаурцеусераусентикатионрекуиред**</span><span class="sxs-lookup"><span data-stu-id="645b6-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-204">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-206">Указывает, настроено ли свойство **усераусентикатионрекуиред** сервером по групповой политике или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="645b6-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="645b6-207">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="645b6-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-208">Сервер</span><span class="sxs-lookup"><span data-stu-id="645b6-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="645b6-209">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="645b6-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-210">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="645b6-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="645b6-211">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="645b6-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-212">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="645b6-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-213">**секуритилайер**</span><span class="sxs-lookup"><span data-stu-id="645b6-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-214">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645b6-216">Квалификаторы: **рдпсекуритилайер** ("уровень безопасности RDP: обмен данными между серверанд, который клиент будет использовать как собственное шифрование RDP"), **согласовывать** ("наиболее безопасный уровень, поддерживаемый клиентом, будет использоваться. Если поддерживается, будет использоваться протокол TLS 1,0. "), **SSL** (" SSL (TLS 1,0) "будет использоваться для проверки подлинности сервера, а также форенкриптинг все данные, передаваемые между сервером и клиентом. Для этого параметра требуется, чтобы сервер имел сертификат, совместимый с SSL. "), **невтбд** (" новый уровень безопасности в LONGHORN ").</span><span class="sxs-lookup"><span data-stu-id="645b6-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="645b6-217">Указывает уровень безопасности, используемый между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="645b6-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="645b6-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Уровень безопасности RDP** (1)</span><span class="sxs-lookup"><span data-stu-id="645b6-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-219">При обмене данными между сервером и клиентом используется собственное шифрование RDP.</span><span class="sxs-lookup"><span data-stu-id="645b6-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="645b6-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Согласование** (2)</span><span class="sxs-lookup"><span data-stu-id="645b6-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-221">Используется наиболее безопасный уровень, поддерживаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="645b6-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="645b6-222">Если поддерживается, используется протокол SSL (TLS 1,0).</span><span class="sxs-lookup"><span data-stu-id="645b6-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="645b6-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span><span class="sxs-lookup"><span data-stu-id="645b6-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-224">Протокол SSL (TLS 1,0) используется для проверки подлинности сервера и для шифрования всех данных, передаваемых между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="645b6-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="645b6-225">Для этого параметра требуется, чтобы сервер имел сертификат, совместимый с SSL.</span><span class="sxs-lookup"><span data-stu-id="645b6-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="645b6-226">Этот параметр несовместим со значением **миненкриптионлевел** , равное 1.</span><span class="sxs-lookup"><span data-stu-id="645b6-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="645b6-227"><span id="NEWTBD"></span><span id="newtbd"></span>**Невтбд** (4)</span><span class="sxs-lookup"><span data-stu-id="645b6-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-228">Новый уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="645b6-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="645b6-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-231">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="645b6-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="645b6-232">Указывает хэш SHA1 в шестнадцатеричном формате SSL-сертификата, который будет использоваться целевым сервером.</span><span class="sxs-lookup"><span data-stu-id="645b6-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="645b6-233">Отпечаток сертификата можно найти с помощью оснастки MMC "сертификаты" на вкладке "сведения" на странице свойств сертификата.</span><span class="sxs-lookup"><span data-stu-id="645b6-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="645b6-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="645b6-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-235">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-237">Указывает состояние свойства **SSLCertificateSHA1Hash** .</span><span class="sxs-lookup"><span data-stu-id="645b6-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="645b6-238">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="645b6-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-239">Недопустимый</span><span class="sxs-lookup"><span data-stu-id="645b6-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="645b6-240">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="645b6-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-241">Самозаверяющий по умолчанию</span><span class="sxs-lookup"><span data-stu-id="645b6-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="645b6-242">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="645b6-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-243">Применение групповой политики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="645b6-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="645b6-244">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="645b6-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="645b6-245">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="645b6-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-246">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="645b6-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645b6-249">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="645b6-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="645b6-250">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="645b6-250">Current status of the object.</span></span> <span data-ttu-id="645b6-251">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="645b6-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="645b6-252">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="645b6-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="645b6-253">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="645b6-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="645b6-254">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="645b6-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="645b6-255">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="645b6-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="645b6-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="645b6-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="645b6-257">("ОК")</span><span class="sxs-lookup"><span data-stu-id="645b6-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-258">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="645b6-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-259">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="645b6-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-260">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="645b6-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-261">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="645b6-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-262">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="645b6-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-263">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="645b6-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="645b6-264">("Служба")</span><span class="sxs-lookup"><span data-stu-id="645b6-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-265">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="645b6-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-266">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-268">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="645b6-268">The name of the terminal.</span></span>

<span data-ttu-id="645b6-269">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="645b6-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="645b6-270">**терминалпротокол**</span><span class="sxs-lookup"><span data-stu-id="645b6-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-273">Имя протокола уровня сеанса; Например, Microsoft RDP 5,0.</span><span class="sxs-lookup"><span data-stu-id="645b6-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="645b6-274">**Транспорт**</span><span class="sxs-lookup"><span data-stu-id="645b6-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="645b6-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-277">Тип транспорта, используемый в соединении; Например, TCP, NetBIOS или IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="645b6-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="645b6-278">**усераусентикатионрекуиред**</span><span class="sxs-lookup"><span data-stu-id="645b6-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-279">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="645b6-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="645b6-281">Указывает тип проверки подлинности пользователя, используемой для удаленных соединений.</span><span class="sxs-lookup"><span data-stu-id="645b6-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="645b6-282">Если задано значение 1, то **усераусентикатионрекуиред** требует проверки подлинности пользователя во время подключения, чтобы повысить защиту сервера от сетевых атак.</span><span class="sxs-lookup"><span data-stu-id="645b6-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="645b6-283">Подключаться могут только клиенты [протокол удаленного рабочего стола](remote-desktop-protocol.md) (RDP), поддерживающие rdp версии 6,0 или выше.</span><span class="sxs-lookup"><span data-stu-id="645b6-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="645b6-284">Чтобы избежать нарушений работы удаленных пользователей, перед включением свойства рекомендуется развернуть клиенты RDP, поддерживающие соответствующую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="645b6-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="645b6-285">Чтобы включить или отключить это свойство, используйте метод [**сетусераусентикатионрекуиред**](setuserauthenticationrequired-win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="645b6-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="645b6-286"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="645b6-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-287">Проверка подлинности пользователя при подключении отключена.</span><span class="sxs-lookup"><span data-stu-id="645b6-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="645b6-288"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="645b6-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-289">Проверка подлинности пользователя при подключении включена.</span><span class="sxs-lookup"><span data-stu-id="645b6-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="645b6-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="645b6-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645b6-291">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645b6-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645b6-292">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="645b6-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="645b6-293">Указывает, является ли соединение стандартным процессом проверки подлинности Windows или другим пакетом проверки подлинности, установленным в системе.</span><span class="sxs-lookup"><span data-stu-id="645b6-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="645b6-294"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="645b6-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-295">Не используется по умолчанию для стандартного процесса проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="645b6-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="645b6-296"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="645b6-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="645b6-297">По умолчанию используется стандартный процесс проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="645b6-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="645b6-298">Комментарии</span><span class="sxs-lookup"><span data-stu-id="645b6-298">Remarks</span></span>

<span data-ttu-id="645b6-299">Имейте в виду, что Windows станции, не связанные с сеансом консоли, не могут получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="645b6-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="645b6-300">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства Терминалнаме, методы этого объекта будут возвращать **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="645b6-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="645b6-301">Этот код ошибки также будет возвращен, если станция Windows пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="645b6-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="645b6-302">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="645b6-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="645b6-303">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="645b6-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="645b6-304">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="645b6-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="645b6-305">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="645b6-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="645b6-306">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="645b6-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="645b6-307">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="645b6-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="645b6-308">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="645b6-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="645b6-309">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="645b6-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="645b6-310">Требования</span><span class="sxs-lookup"><span data-stu-id="645b6-310">Requirements</span></span>



| <span data-ttu-id="645b6-311">Требование</span><span class="sxs-lookup"><span data-stu-id="645b6-311">Requirement</span></span> | <span data-ttu-id="645b6-312">Значение</span><span class="sxs-lookup"><span data-stu-id="645b6-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="645b6-313">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="645b6-313">Minimum supported client</span></span><br/> | <span data-ttu-id="645b6-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="645b6-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="645b6-315">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="645b6-315">Minimum supported server</span></span><br/> | <span data-ttu-id="645b6-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="645b6-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="645b6-317">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="645b6-317">Namespace</span></span><br/>                | <span data-ttu-id="645b6-318">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="645b6-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="645b6-319">MOF</span><span class="sxs-lookup"><span data-stu-id="645b6-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="645b6-320"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="645b6-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="645b6-321">DLL</span><span class="sxs-lookup"><span data-stu-id="645b6-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="645b6-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="645b6-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="645b6-323">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="645b6-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645b6-324">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="645b6-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

