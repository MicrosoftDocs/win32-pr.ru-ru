---
title: Метод Сетпортнумберс класса Win32_TSGatewayResourceAuthorizationPolicy
description: Задает номера портов, которым разрешено подключаться к ресурсу через шлюз удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпортнумберс
- Службы удаленных рабочих столов метода Сетпортнумберс, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Сетпортнумберс
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491613"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="986a5-106">Метод Сетпортнумберс \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="986a5-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="986a5-107">Задает номера портов, которым разрешено подключаться к ресурсу через шлюз удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="986a5-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="986a5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="986a5-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="986a5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="986a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986a5-110">*Портнумберс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="986a5-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986a5-111">Список номеров портов, разделенных точкой с запятой, которые разрешены для этой удаленный рабочий стол политики авторизации ресурсов (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="986a5-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="986a5-112">Чтобы разрешить любой номер порта, установите " \* ".</span><span class="sxs-lookup"><span data-stu-id="986a5-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="986a5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="986a5-113">Remarks</span></span>

<span data-ttu-id="986a5-114">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="986a5-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="986a5-115">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="986a5-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="986a5-116">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="986a5-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="986a5-117">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="986a5-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="986a5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="986a5-118">Requirements</span></span>



| <span data-ttu-id="986a5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="986a5-119">Requirement</span></span> | <span data-ttu-id="986a5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="986a5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="986a5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="986a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="986a5-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="986a5-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="986a5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="986a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="986a5-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="986a5-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="986a5-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="986a5-125">Namespace</span></span><br/>                | <span data-ttu-id="986a5-126">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="986a5-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="986a5-127">MOF</span><span class="sxs-lookup"><span data-stu-id="986a5-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="986a5-128"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="986a5-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="986a5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="986a5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="986a5-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="986a5-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="986a5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="986a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986a5-132">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="986a5-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

