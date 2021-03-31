---
title: Структура MCI_VCR_SETTUNER_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс СЕТТУНЕР видеомагнитофона MCI \_ содержит параметры для \_ команды MCI сеттунер для устройств записи видеокассет.'
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- MCI_VCR_SETTUNER_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802501"
---
# <a name="mci_vcr_settuner_parms-structure"></a><span data-ttu-id="ce447-104">\_Структура пармс видеомагнитофона MCI \_ сеттунер \_</span><span class="sxs-lookup"><span data-stu-id="ce447-104">MCI\_VCR\_SETTUNER\_PARMS structure</span></span>

<span data-ttu-id="ce447-105">Структура **\_ \_ \_ пармс сеттунер видеомагнитофона MCI** содержит параметры для команды [**MCI \_ сеттунер**](mci-settuner.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="ce447-105">The **MCI\_VCR\_SETTUNER\_PARMS** structure contains parameters for the [**MCI\_SETTUNER**](mci-settuner.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce447-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce447-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a><span data-ttu-id="ce447-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ce447-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce447-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="ce447-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ce447-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="ce447-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ce447-110">**двчаннел**</span><span class="sxs-lookup"><span data-stu-id="ce447-110">**dwChannel**</span></span>
</dt> <dd>

<span data-ttu-id="ce447-111">Номер нового канала.</span><span class="sxs-lookup"><span data-stu-id="ce447-111">New channel number.</span></span>

</dd> <dt>

<span data-ttu-id="ce447-112">**двнумбер**</span><span class="sxs-lookup"><span data-stu-id="ce447-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ce447-113">Логический тюнер, на который влияет команда [**MCI \_ сеттунер**](mci-settuner.md) .</span><span class="sxs-lookup"><span data-stu-id="ce447-113">Logical tuner that the [**MCI\_SETTUNER**](mci-settuner.md) command affects.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce447-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce447-114">Remarks</span></span>

<span data-ttu-id="ce447-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="ce447-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce447-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ce447-116">Requirements</span></span>



| <span data-ttu-id="ce447-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ce447-117">Requirement</span></span> | <span data-ttu-id="ce447-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ce447-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ce447-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce447-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce447-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce447-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ce447-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce447-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce447-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce447-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce447-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ce447-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce447-124"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce447-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce447-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce447-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce447-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ce447-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ce447-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="ce447-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ce447-128">**\_СЕТТУНЕР MCI**</span><span class="sxs-lookup"><span data-stu-id="ce447-128">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
</dt> <dt>

<span data-ttu-id="ce447-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce447-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

