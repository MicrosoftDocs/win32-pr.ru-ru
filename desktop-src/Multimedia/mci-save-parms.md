---
title: Структура MCI_SAVE_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс для сохранения данных содержит сведения о имени файла для \_ команды MCI Save.'
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- MCI_SAVE_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672531"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="aa42b-104">\_Структура для сохранения пармс в MCI \_</span><span class="sxs-lookup"><span data-stu-id="aa42b-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="aa42b-105">Структура **\_ \_ пармс для сохранения** данных содержит сведения о имени файла для команды [**MCI \_ Save**](mci-save.md) .</span><span class="sxs-lookup"><span data-stu-id="aa42b-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa42b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa42b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="aa42b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="aa42b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa42b-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="aa42b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="aa42b-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="aa42b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="aa42b-110">**лпфиленаме**</span><span class="sxs-lookup"><span data-stu-id="aa42b-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="aa42b-111">Имя сохраняемого файла.</span><span class="sxs-lookup"><span data-stu-id="aa42b-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa42b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa42b-112">Remarks</span></span>

<span data-ttu-id="aa42b-113">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="aa42b-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa42b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aa42b-114">Requirements</span></span>



| <span data-ttu-id="aa42b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aa42b-115">Requirement</span></span> | <span data-ttu-id="aa42b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aa42b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa42b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa42b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa42b-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa42b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aa42b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa42b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa42b-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa42b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aa42b-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aa42b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa42b-122"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa42b-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa42b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa42b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa42b-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="aa42b-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="aa42b-125">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="aa42b-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="aa42b-126">**\_Сохранение MCI**</span><span class="sxs-lookup"><span data-stu-id="aa42b-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="aa42b-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa42b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

