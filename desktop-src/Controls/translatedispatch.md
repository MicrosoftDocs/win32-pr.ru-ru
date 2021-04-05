---
title: Функция обратного вызова Транслатедиспатч
description: Используется клиентом функции Дореадермоде для перехвата и явной обработки сообщений Windows, предназначенных для области прокрутки окна режима чтения. Это функция обратного вызова, определяемая приложением.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Элементы управления Windows для функции обратного вызова Транслатедиспатч
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988544"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="232f1-105">Функция обратного вызова Транслатедиспатч</span><span class="sxs-lookup"><span data-stu-id="232f1-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="232f1-106">\[*Транслатедиспатч* доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="232f1-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="232f1-107">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="232f1-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="232f1-108">Используется клиентом функции [**дореадермоде**](doreadermode.md) для перехвата и явной обработки сообщений Windows, предназначенных для области прокрутки окна режима чтения.</span><span class="sxs-lookup"><span data-stu-id="232f1-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="232f1-109">Это функция обратного вызова, определяемая приложением.</span><span class="sxs-lookup"><span data-stu-id="232f1-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="232f1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="232f1-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="232f1-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="232f1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="232f1-112">*лпмсг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="232f1-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="232f1-113">Тип: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="232f1-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="232f1-114">Указатель на структуру [_ *MSG* \*](/windows/win32/api/winuser/ns-winuser-msg) , содержащую перехваченное сообщение.</span><span class="sxs-lookup"><span data-stu-id="232f1-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="232f1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="232f1-115">Return value</span></span>

<span data-ttu-id="232f1-116">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="232f1-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="232f1-117">**Значение true** , если сообщение было обработано этой функцией; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="232f1-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="232f1-118">Если **значение равно false**, сообщение обрабатывается реализацией режима модуля чтения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="232f1-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="232f1-119">Эта реализация обрабатывает перемещение и кнопки мыши, а также клавиши.</span><span class="sxs-lookup"><span data-stu-id="232f1-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="232f1-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="232f1-120">Examples</span></span>

<span data-ttu-id="232f1-121">В следующем примере демонстрируется реализация этой функции.</span><span class="sxs-lookup"><span data-stu-id="232f1-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="232f1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="232f1-122">Requirements</span></span>



| <span data-ttu-id="232f1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="232f1-123">Requirement</span></span> | <span data-ttu-id="232f1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="232f1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="232f1-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="232f1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="232f1-126">Windows Vista, \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="232f1-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="232f1-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="232f1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="232f1-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="232f1-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

