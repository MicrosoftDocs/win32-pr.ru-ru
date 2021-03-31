---
title: Метод Сетсекуритилайер класса Win32_TSGeneralSetting
description: Метод Сетсекуритилайер задает уровень безопасности.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсекуритилайер
- Службы удаленных рабочих столов метода Сетсекуритилайер, класс Win32_TSGeneralSetting
- Класс Win32_TSGeneralSetting службы удаленных рабочих столов, метод Сетсекуритилайер
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988754"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="670a2-106">Метод Сетсекуритилайер \_ класса Win32 тсженералсеттинг</span><span class="sxs-lookup"><span data-stu-id="670a2-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="670a2-107">Метод **сетсекуритилайер** задает уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="670a2-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="670a2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="670a2-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="670a2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="670a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670a2-110">*Секуритилайер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="670a2-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="670a2-111">Устанавливаемый уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="670a2-111">The security layer to set.</span></span> <span data-ttu-id="670a2-112">Если текущий уровень шифрования равен 1, то недопустимо значение 2 для *секуритилайер* .</span><span class="sxs-lookup"><span data-stu-id="670a2-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="670a2-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Уровень безопасности RDP** (0)</span><span class="sxs-lookup"><span data-stu-id="670a2-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="670a2-114">Связь между сервером и клиентом будет использовать собственное шифрование RDP.</span><span class="sxs-lookup"><span data-stu-id="670a2-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="670a2-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Согласование** (1)</span><span class="sxs-lookup"><span data-stu-id="670a2-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="670a2-116">Будет использоваться наиболее безопасный уровень, поддерживаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="670a2-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="670a2-117">Если поддерживается, будет использоваться протокол SSL (TLS 1,0).</span><span class="sxs-lookup"><span data-stu-id="670a2-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="670a2-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span><span class="sxs-lookup"><span data-stu-id="670a2-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="670a2-119">Протокол SSL (TLS 1,0) будет использоваться для проверки подлинности сервера, а также для шифрования всех данных, передаваемых между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="670a2-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="670a2-120">Для этого параметра требуется, чтобы сервер имел сертификат, совместимый с SSL.</span><span class="sxs-lookup"><span data-stu-id="670a2-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="670a2-121">Этот параметр несовместим со значением **миненкриптионлевел** , равное 1.</span><span class="sxs-lookup"><span data-stu-id="670a2-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670a2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="670a2-122">Return value</span></span>

<span data-ttu-id="670a2-123">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="670a2-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="670a2-124">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="670a2-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="670a2-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="670a2-125">Remarks</span></span>

<span data-ttu-id="670a2-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="670a2-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="670a2-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="670a2-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="670a2-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="670a2-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="670a2-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="670a2-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="670a2-130">Требования</span><span class="sxs-lookup"><span data-stu-id="670a2-130">Requirements</span></span>



| <span data-ttu-id="670a2-131">Требование</span><span class="sxs-lookup"><span data-stu-id="670a2-131">Requirement</span></span> | <span data-ttu-id="670a2-132">Значение</span><span class="sxs-lookup"><span data-stu-id="670a2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="670a2-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="670a2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="670a2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="670a2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="670a2-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="670a2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="670a2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="670a2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="670a2-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="670a2-137">Namespace</span></span><br/>                | <span data-ttu-id="670a2-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="670a2-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="670a2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="670a2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="670a2-140"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="670a2-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="670a2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="670a2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="670a2-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="670a2-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670a2-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="670a2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670a2-144">**\_Тсженералсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="670a2-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="670a2-145">**сетенкриптионлевел**</span><span class="sxs-lookup"><span data-stu-id="670a2-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

