---
title: Структура MCI_SYSINFO_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI сисинфо содержит сведения для \_ команды MCI сисинфо.'
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672461"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="b9aad-104">\_ \_ Структура пармс MCI сисинфо</span><span class="sxs-lookup"><span data-stu-id="b9aad-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="b9aad-105">Структура **\_ \_ пармс MCI сисинфо** содержит сведения для команды [**MCI \_ сисинфо**](mci-sysinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="b9aad-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9aad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9aad-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="b9aad-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b9aad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9aad-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b9aad-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="b9aad-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b9aad-110">**лпстрретурн**</span><span class="sxs-lookup"><span data-stu-id="b9aad-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-111">Указатель на предоставляемый пользователем буфер для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="b9aad-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="b9aad-112">Он также используется для возврата значения **DWORD** при \_ \_ использовании флага MCI сисинфо Quantity.</span><span class="sxs-lookup"><span data-stu-id="b9aad-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="b9aad-113">**двретсизе**</span><span class="sxs-lookup"><span data-stu-id="b9aad-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-114">Размер буфера возврата в байтах.</span><span class="sxs-lookup"><span data-stu-id="b9aad-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b9aad-115">**двнумбер**</span><span class="sxs-lookup"><span data-stu-id="b9aad-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-116">Число, указывающее расположение устройства в таблице устройства MCI или в списке открытых устройств, если \_ \_ установлен флаг открытия MCI сисинфо.</span><span class="sxs-lookup"><span data-stu-id="b9aad-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="b9aad-117">**вдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="b9aad-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-118">Тип устройства.</span><span class="sxs-lookup"><span data-stu-id="b9aad-118">Type of device.</span></span> <span data-ttu-id="b9aad-119">Этот элемент может быть одним из значений, перечисленных в [типах устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="b9aad-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9aad-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9aad-120">Remarks</span></span>

<span data-ttu-id="b9aad-121">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="b9aad-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9aad-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b9aad-122">Requirements</span></span>



| <span data-ttu-id="b9aad-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b9aad-123">Requirement</span></span> | <span data-ttu-id="b9aad-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b9aad-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b9aad-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9aad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b9aad-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9aad-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9aad-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9aad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b9aad-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9aad-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b9aad-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9aad-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9aad-130"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9aad-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9aad-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9aad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9aad-132">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b9aad-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b9aad-133">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="b9aad-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b9aad-134">**\_СИСИНФО MCI**</span><span class="sxs-lookup"><span data-stu-id="b9aad-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="b9aad-135">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9aad-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

