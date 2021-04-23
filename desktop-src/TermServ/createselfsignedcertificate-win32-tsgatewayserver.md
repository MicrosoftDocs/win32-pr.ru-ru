---
title: Метод Креатеселфсигнедцертификате класса Win32_TSGatewayServer
description: Создает самозаверяющий сертификат и возвращает хэш сертификата в виде \ 0034; out \ 0034; параметр.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатеселфсигнедцертификате
- Службы удаленных рабочих столов метода Креатеселфсигнедцертификате, класс Win32_TSGatewayServer
- Класс Win32_TSGatewayServer службы удаленных рабочих столов, метод Креатеселфсигнедцертификате
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489531"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="60fab-106">Метод Креатеселфсигнедцертификате \_ класса Win32 тсгатевайсервер</span><span class="sxs-lookup"><span data-stu-id="60fab-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="60fab-107">Создает самозаверяющий сертификат и возвращает хэш сертификата как параметр "out".</span><span class="sxs-lookup"><span data-stu-id="60fab-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="60fab-108">Кроме того, добавляет текст " \_ самозаверяющий сертификат шлюза TS \_ \_ \_ " в свойство контекста сертификата, чтобы сертификат был распознан как сертификат шлюза удаленный рабочий стол шлюза.</span><span class="sxs-lookup"><span data-stu-id="60fab-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="60fab-109">Этот метод использует контейнер ключей для конкретного шлюза удаленных рабочих столов, чтобы создать сертификат.</span><span class="sxs-lookup"><span data-stu-id="60fab-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fab-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60fab-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="60fab-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="60fab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60fab-112">*SubjectName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60fab-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60fab-113">Имя субъекта самозаверяющего сертификата.</span><span class="sxs-lookup"><span data-stu-id="60fab-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="60fab-114">*CertHash* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60fab-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60fab-115">Хэш сертификата.</span><span class="sxs-lookup"><span data-stu-id="60fab-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60fab-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60fab-116">Remarks</span></span>

<span data-ttu-id="60fab-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="60fab-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="60fab-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="60fab-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60fab-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="60fab-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60fab-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="60fab-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60fab-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60fab-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60fab-122">Требования</span><span class="sxs-lookup"><span data-stu-id="60fab-122">Requirements</span></span>



| <span data-ttu-id="60fab-123">Требование</span><span class="sxs-lookup"><span data-stu-id="60fab-123">Requirement</span></span> | <span data-ttu-id="60fab-124">Значение</span><span class="sxs-lookup"><span data-stu-id="60fab-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60fab-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60fab-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60fab-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60fab-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="60fab-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60fab-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60fab-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60fab-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="60fab-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60fab-129">Namespace</span></span><br/>                | <span data-ttu-id="60fab-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="60fab-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="60fab-131">MOF</span><span class="sxs-lookup"><span data-stu-id="60fab-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60fab-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60fab-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="60fab-133">DLL</span><span class="sxs-lookup"><span data-stu-id="60fab-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60fab-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60fab-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="60fab-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60fab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fab-136">**\_Тсгатевайсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="60fab-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

