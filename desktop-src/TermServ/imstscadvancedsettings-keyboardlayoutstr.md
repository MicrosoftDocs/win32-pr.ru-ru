---
title: Имстскадванцедсеттингс Кэйбоардлайаутстр, свойство
description: Задает имя активного идентификатора языка ввода (прежнее название раскладки клавиатуры), используемого для соединения.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Кэйбоардлайаутстр
- Службы удаленных рабочих столов свойства Кэйбоардлайаутстр, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Кэйбоардлайаутстр
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802278"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="7663f-106">Свойство Имстскадванцедсеттингс:: Кэйбоардлайаутстр</span><span class="sxs-lookup"><span data-stu-id="7663f-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="7663f-107">Задает имя активного идентификатора языка ввода (прежнее название раскладки клавиатуры), используемого для соединения.</span><span class="sxs-lookup"><span data-stu-id="7663f-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="7663f-108">Если это свойство не задано, элемент управления использует макет по умолчанию, возвращаемый функцией [**жеткэйбоардлайаут**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .</span><span class="sxs-lookup"><span data-stu-id="7663f-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="7663f-109">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="7663f-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7663f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7663f-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="7663f-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7663f-111">Property value</span></span>

<span data-ttu-id="7663f-112">Имя активного идентификатора языка ввода.</span><span class="sxs-lookup"><span data-stu-id="7663f-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7663f-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7663f-113">Error codes</span></span>

<span data-ttu-id="7663f-114">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="7663f-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7663f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7663f-115">Remarks</span></span>

<span data-ttu-id="7663f-116">Свойство является шестнадцатеричным числом из восьми цифр в форме строки.</span><span class="sxs-lookup"><span data-stu-id="7663f-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="7663f-117">Младшие четыре цифры обозначают идентификатор языка, а верхние четыре цифры обозначают вариант клавиатуры на этом языке.</span><span class="sxs-lookup"><span data-stu-id="7663f-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="7663f-118">Например, "00000409" представляет стандартную клавиатуру США по умолчанию, так как "0409" является идентификатором английского языка (США).</span><span class="sxs-lookup"><span data-stu-id="7663f-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="7663f-119">Вариант по Двораку английской клавиатуры США имеет идентификатор "00010409".</span><span class="sxs-lookup"><span data-stu-id="7663f-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="7663f-120">Доступные раскладки клавиатуры, перечисленные по идентификаторам раскладки клавиатуры, можно найти в реестре в разделе</span><span class="sxs-lookup"><span data-stu-id="7663f-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="7663f-121">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7663f-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7663f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7663f-122">Requirements</span></span>



| <span data-ttu-id="7663f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7663f-123">Requirement</span></span> | <span data-ttu-id="7663f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7663f-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7663f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7663f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7663f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7663f-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="7663f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7663f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7663f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7663f-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7663f-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7663f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="7663f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7663f-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7663f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7663f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7663f-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7663f-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7663f-133">IID</span><span class="sxs-lookup"><span data-stu-id="7663f-133">IID</span></span><br/>                      | <span data-ttu-id="7663f-134">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="7663f-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7663f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7663f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7663f-136">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="7663f-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

