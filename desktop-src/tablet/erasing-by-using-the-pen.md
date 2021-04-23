---
description: Если вы решили реализовать стирание в приложении, отличном от, с помощью объекта InkOverlay, это можно сделать с помощью одного из следующих двух методов.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Стирание с помощью пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423789"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="67758-103">Стирание с помощью пера</span><span class="sxs-lookup"><span data-stu-id="67758-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="67758-104">Если вы решили реализовать стирание в приложении, отличном от, с помощью объекта [**InkOverlay**](inkoverlay-class.md) , это можно сделать с помощью одного из следующих двух методов.</span><span class="sxs-lookup"><span data-stu-id="67758-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="67758-105">Использование кончика пера</span><span class="sxs-lookup"><span data-stu-id="67758-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="67758-106">Совет планшетного пера обычно используется для рукописного ввода и рисования. Однако TIP можно также использовать для стирания рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="67758-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="67758-107">Для этого приложение должно иметь режим стирания, который пользователи могут использовать.</span><span class="sxs-lookup"><span data-stu-id="67758-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="67758-108">В этом режиме используйте проверку нажатия для определения рукописных данных, на которые курсор перемещается.</span><span class="sxs-lookup"><span data-stu-id="67758-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="67758-109">Можно установить режим стирания, чтобы удалить только рукописные данные, передаваемые курсором, или целые фрагменты, пересекающие путь курсора, в зависимости от особенностей проектирования и функциональности.</span><span class="sxs-lookup"><span data-stu-id="67758-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="67758-110">Пример использования режима стирания для стирания рукописного ввода см. в [примере стирания рукописного ввода](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="67758-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="67758-111">Использование верхней части пера</span><span class="sxs-lookup"><span data-stu-id="67758-111">Using the Top of the Pen</span></span>

<span data-ttu-id="67758-112">Чтобы реализовать стирание с помощью верхней части пера планшета, приложение должно искать изменения в курсоре.</span><span class="sxs-lookup"><span data-stu-id="67758-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="67758-113">Чтобы найти инвертированный курсор, прослушайте событие [**курсоринранже**](inkoverlay-cursorinrange.md) , чтобы определить, находится ли курсор в контексте приложения.</span><span class="sxs-lookup"><span data-stu-id="67758-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="67758-114">Если курсор находится в диапазоне, найдите [**Инвертированное**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) свойство в объекте [**курсора**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="67758-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="67758-115">Если **Инвертированное** свойство имеет **значение true**, выполните проверку нажатия, чтобы определить, на какие рукописные данные перемещается курсор.</span><span class="sxs-lookup"><span data-stu-id="67758-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="67758-116">Удалите рукописный ввод или штрихи, пересекающие путь курсора, в зависимости от особенностей проектирования и функциональности.</span><span class="sxs-lookup"><span data-stu-id="67758-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="67758-117">Пример использования верхней части пера для стирания рукописного ввода см. в [примере стирания рукописного ввода](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="67758-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="67758-118">Определение, включено ли стирание с помощью верхней части пера</span><span class="sxs-lookup"><span data-stu-id="67758-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="67758-119">Пользователи могут использовать верхушку пера, чтобы стереть рукописные данные в приложениях, предназначенных для планшетных ПК, если они допускают их конкретное оборудование.</span><span class="sxs-lookup"><span data-stu-id="67758-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="67758-120">Доступ к этой функции осуществляется с помощью флажка в поле Группа кнопок пера на вкладке Параметры пера диалогового окна Панель управления планшета и настройки пера.</span><span class="sxs-lookup"><span data-stu-id="67758-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="67758-121">Чтобы определить, включил ли пользователь стирание в начало пера, проверьте следующий подраздел реестра:</span><span class="sxs-lookup"><span data-stu-id="67758-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="67758-122">`EraseEnable`Запись этого подраздела имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="67758-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="67758-123">Значение этой записи равно 1 для параметра включено или 0 для параметра отключено.</span><span class="sxs-lookup"><span data-stu-id="67758-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="67758-124">Другие значения зарезервированы для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="67758-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="67758-125">Если приложение позволяет использовать верхушку пера для стирания, следует проверить и кэшировать значение записи Ерасинабле в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="67758-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="67758-126">Запустится приложение.</span><span class="sxs-lookup"><span data-stu-id="67758-126">Your application launches.</span></span>
-   <span data-ttu-id="67758-127">Всякий раз, когда приложение получает фокус после потери фокуса.</span><span class="sxs-lookup"><span data-stu-id="67758-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="67758-128">Используйте это кэшированное значение, чтобы соответствующим образом изменить поведение приложения.</span><span class="sxs-lookup"><span data-stu-id="67758-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="67758-129">В следующем примере на языке C \# определяется `GetEraseEnabled` метод, который проверяет значение `EraseEnable` записи в `SysEventParameters` подразделе.</span><span class="sxs-lookup"><span data-stu-id="67758-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="67758-130">`GetEraseEnabled`Метод возвращает значение **true** , если значение записи равно 1; возвращает значение **false** , если значение записи равно 0, или вызывает исключение [InvalidOperationException](/dotnet/api/system.invalidoperationexception) , если значение записи отлично от 1 или 0.</span><span class="sxs-lookup"><span data-stu-id="67758-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="67758-131">`GetEraseEnabled`Метод возвращает ожидаемое значение **true** , если не указан подраздел или запись.</span><span class="sxs-lookup"><span data-stu-id="67758-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
