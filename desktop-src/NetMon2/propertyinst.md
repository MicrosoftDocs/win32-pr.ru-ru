---
description: Структура ПРОПЕРТИНСТ определяет экземпляр свойства в части распознаваемых данных. Сетевой монитор выделяет и заполняет структуру ПРОПЕРТИНСТ, когда свойство прикрепляется к записи.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Структура ПРОПЕРТИНСТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662896"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="d885f-104">Структура ПРОПЕРТИНСТ</span><span class="sxs-lookup"><span data-stu-id="d885f-104">PROPERTYINST structure</span></span>

<span data-ttu-id="d885f-105">Структура **пропертинст** определяет экземпляр свойства в части распознаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="d885f-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="d885f-106">Сетевой монитор выделяет и заполняет структуру **пропертинст** , когда свойство прикрепляется к записи.</span><span class="sxs-lookup"><span data-stu-id="d885f-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d885f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d885f-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="d885f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d885f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d885f-109">**лппропертинфо**</span><span class="sxs-lookup"><span data-stu-id="d885f-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-110">Указатель на структуру [PROPERTYINFO](propertyinfo.md) , определяющую свойство.</span><span class="sxs-lookup"><span data-stu-id="d885f-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-111">**сзпропертитекст**</span><span class="sxs-lookup"><span data-stu-id="d885f-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-112">Указатель на строку, которая отображается в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="d885f-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-113">**лпдата**</span><span class="sxs-lookup"><span data-stu-id="d885f-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-114">Указатель на начало данных для свойства.</span><span class="sxs-lookup"><span data-stu-id="d885f-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="d885f-115">Средство синтаксического анализа определяет, откуда запускаются данные свойства.</span><span class="sxs-lookup"><span data-stu-id="d885f-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-116">**lpByte**</span><span class="sxs-lookup"><span data-stu-id="d885f-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-117">Указатель на **байтовые** данные.</span><span class="sxs-lookup"><span data-stu-id="d885f-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-118">**лпворд**</span><span class="sxs-lookup"><span data-stu-id="d885f-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-119">Указатель на данные **слова** .</span><span class="sxs-lookup"><span data-stu-id="d885f-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-120">**лпдворд**</span><span class="sxs-lookup"><span data-stu-id="d885f-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-121">Указатель на данные **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d885f-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-122">**лпларжеинт**</span><span class="sxs-lookup"><span data-stu-id="d885f-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-123">Указатель на данные [**ларжеинт**](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="d885f-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-124">**лпсистиме**</span><span class="sxs-lookup"><span data-stu-id="d885f-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-125">Указатель на данные [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="d885f-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-126">**лппропертинстекс**</span><span class="sxs-lookup"><span data-stu-id="d885f-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-127">Указатель на структуру [пропертинстекс](propertyinstex.md) .</span><span class="sxs-lookup"><span data-stu-id="d885f-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="d885f-128">Элемент **лппропертинстекс** используется только при вызове [аттачпропертинстанцеекс](attachpropertyinstanceex.md).</span><span class="sxs-lookup"><span data-stu-id="d885f-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="d885f-129">Если используется **лппропертинстекс** , необходимо задать для элемента **DATALENGTH** значение 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="d885f-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-130">**DataLength**</span><span class="sxs-lookup"><span data-stu-id="d885f-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-131">Длина данных для этого экземпляра свойства.</span><span class="sxs-lookup"><span data-stu-id="d885f-131">Data length for this instance of the property.</span></span> <span data-ttu-id="d885f-132">Если элемент **лппропертинстекс** указывает на структуру [**пропертинстекс**](propertyinstex.md) , необходимо установить параметр **DATALENGTH** в значение 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="d885f-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-133">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="d885f-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-134">Сведения об уровне.</span><span class="sxs-lookup"><span data-stu-id="d885f-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-135">**Идентификатор справки**</span><span class="sxs-lookup"><span data-stu-id="d885f-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-136">Идентификатор контекста файла справки.</span><span class="sxs-lookup"><span data-stu-id="d885f-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d885f-137">**ифлагс**</span><span class="sxs-lookup"><span data-stu-id="d885f-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d885f-138">Флаг условия ошибки.</span><span class="sxs-lookup"><span data-stu-id="d885f-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d885f-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d885f-139">Remarks</span></span>

<span data-ttu-id="d885f-140">Структура **пропертинст** определяет экземпляр присоединенного свойства.</span><span class="sxs-lookup"><span data-stu-id="d885f-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="d885f-141">Средство синтаксического анализа обращается к структуре **пропертинст** через несколько вспомогательных функций.</span><span class="sxs-lookup"><span data-stu-id="d885f-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="d885f-142">Например, при вызове функции [**форматпропертинстанце**](formatpropertyinstance.md) для форматирования данных свойства он изменяет элемент **сзпропертитекст** структуры **пропертинст** .</span><span class="sxs-lookup"><span data-stu-id="d885f-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d885f-143">Требования</span><span class="sxs-lookup"><span data-stu-id="d885f-143">Requirements</span></span>



| <span data-ttu-id="d885f-144">Требование</span><span class="sxs-lookup"><span data-stu-id="d885f-144">Requirement</span></span> | <span data-ttu-id="d885f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="d885f-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d885f-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d885f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d885f-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d885f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d885f-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d885f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d885f-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d885f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d885f-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d885f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d885f-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d885f-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d885f-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d885f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d885f-153">аттачпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="d885f-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="d885f-154">аттачпропертинстанцеекс</span><span class="sxs-lookup"><span data-stu-id="d885f-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

