---
description: Структура МКСДК \_ Get \_ filename \_ Data \_ T содержит полный путь и имя выходного файла конвертера документов Microsoft XPS (мксдк).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Структура MXDC_GET_FILENAME_DATA_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909580"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="972fd-103">МКСДК \_ получить \_ \_ структуру данных имени файла \_ T</span><span class="sxs-lookup"><span data-stu-id="972fd-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="972fd-104">Структура **мксдк \_ Get \_ filename \_ Data \_ T** содержит полный путь и имя выходного файла конвертера документов Microsoft XPS (мксдк).</span><span class="sxs-lookup"><span data-stu-id="972fd-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="972fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="972fd-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="972fd-106">Члены</span><span class="sxs-lookup"><span data-stu-id="972fd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="972fd-107">**кбаутпут**</span><span class="sxs-lookup"><span data-stu-id="972fd-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="972fd-108">Размер выходного буфера **всздата**.</span><span class="sxs-lookup"><span data-stu-id="972fd-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="972fd-109">**всздата**</span><span class="sxs-lookup"><span data-stu-id="972fd-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="972fd-110">Полный путь и имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="972fd-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="972fd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="972fd-111">Remarks</span></span>

<span data-ttu-id="972fd-112">Эта структура возвращается функцией [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , когда она вызывается с помощью escape-последовательности [**мксдк \_**](mxdc-escape.md) , а структура [**Escape- \_ \_ заголовка \_ мксдк**](mxdcescapeheader.md) , которая передается в параметр *лпсзиндата* , **имеет значение** **мксдкоп \_ Get \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="972fd-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="972fd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="972fd-113">Requirements</span></span>



| <span data-ttu-id="972fd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="972fd-114">Requirement</span></span> | <span data-ttu-id="972fd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="972fd-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="972fd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="972fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="972fd-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="972fd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="972fd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="972fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="972fd-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="972fd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="972fd-120">Header</span><span class="sxs-lookup"><span data-stu-id="972fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="972fd-121"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="972fd-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="972fd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="972fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972fd-123">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="972fd-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="972fd-124">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="972fd-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="972fd-125">[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="972fd-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="972fd-126">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="972fd-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="972fd-127">**Escape-МКСДК \_**</span><span class="sxs-lookup"><span data-stu-id="972fd-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

