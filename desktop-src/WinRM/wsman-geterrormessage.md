---
title: Метод WSMan. Жетеррормессаже (Всмандисп. h)
description: Возвращает отформатированную строку, содержащую текст номера ошибки.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Жетеррормессаже
- Служба удаленного управления Windows метода Жетеррормессаже, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Жетеррормессаже
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340695"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="01620-106">Метод WSMan. Жетеррормессаже</span><span class="sxs-lookup"><span data-stu-id="01620-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="01620-107">Возвращает отформатированную строку, содержащую текст номера ошибки.</span><span class="sxs-lookup"><span data-stu-id="01620-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="01620-108">Этот метод выполняет ту же операцию, что **и в командной строке** WinRM ( **WinRM helpmsg** ) с *десятичным или шестнадцатеричным номером ошибки*.</span><span class="sxs-lookup"><span data-stu-id="01620-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="01620-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01620-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="01620-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="01620-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01620-111">*номер ошибки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01620-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01620-112">Номер сообщения об ошибке в десятичном или шестнадцатеричном формате от WinRM, WinHTTP или других компонентов операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01620-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="01620-113">*ErrorMessage* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="01620-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01620-114">Строка сообщения об ошибке, отформатированная как сообщения, возвращенные командой **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="01620-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01620-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01620-115">Remarks</span></span>

<span data-ttu-id="01620-116">Соответствующий метод C++ — [**ивсманекс:: жетеррормессаже**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span><span class="sxs-lookup"><span data-stu-id="01620-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="01620-117">Требования</span><span class="sxs-lookup"><span data-stu-id="01620-117">Requirements</span></span>



| <span data-ttu-id="01620-118">Требование</span><span class="sxs-lookup"><span data-stu-id="01620-118">Requirement</span></span> | <span data-ttu-id="01620-119">Значение</span><span class="sxs-lookup"><span data-stu-id="01620-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01620-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01620-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01620-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01620-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="01620-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01620-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01620-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01620-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="01620-124">Header</span><span class="sxs-lookup"><span data-stu-id="01620-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01620-125"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="01620-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01620-126">IDL</span><span class="sxs-lookup"><span data-stu-id="01620-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01620-127"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01620-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="01620-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01620-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="01620-129"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01620-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01620-130">DLL</span><span class="sxs-lookup"><span data-stu-id="01620-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01620-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01620-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01620-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01620-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01620-133">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="01620-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





