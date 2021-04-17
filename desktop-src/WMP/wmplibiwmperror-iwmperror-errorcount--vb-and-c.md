---
title: Ивмперрор Ерроркаунт, свойство
description: Свойство Ерроркаунт возвращает количество ошибок в очереди ошибок.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Проигрыватель Windows Media для свойства Ерроркаунт
- Ерроркаунт свойство проигрывателя Windows Media Player, интерфейс Ивмперрор
- Интерфейс Ивмперрор Windows Media Player, свойство Ерроркаунт
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708536"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="651de-106">Свойство Ивмперрор:: Ерроркаунт</span><span class="sxs-lookup"><span data-stu-id="651de-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="651de-107">Свойство **ерроркаунт** возвращает количество ошибок в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="651de-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="651de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="651de-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="651de-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="651de-109">Property value</span></span>

<span data-ttu-id="651de-110">Объект **System. Int32** , который является числом ошибок.</span><span class="sxs-lookup"><span data-stu-id="651de-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="651de-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="651de-111">Remarks</span></span>

<span data-ttu-id="651de-112">Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .</span><span class="sxs-lookup"><span data-stu-id="651de-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="651de-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="651de-113">Examples</span></span>

<span data-ttu-id="651de-114">В следующем примере используется **ерроркаунт** в обработчике событий ошибки, чтобы предупредить пользователя о последней ошибке в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="651de-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="651de-115">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="651de-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="651de-116">Требования</span><span class="sxs-lookup"><span data-stu-id="651de-116">Requirements</span></span>



| <span data-ttu-id="651de-117">Требование</span><span class="sxs-lookup"><span data-stu-id="651de-117">Requirement</span></span> | <span data-ttu-id="651de-118">Значение</span><span class="sxs-lookup"><span data-stu-id="651de-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="651de-119">Версия</span><span class="sxs-lookup"><span data-stu-id="651de-119">Version</span></span><br/>   | <span data-ttu-id="651de-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="651de-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="651de-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="651de-121">Namespace</span></span><br/> | <span data-ttu-id="651de-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="651de-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="651de-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="651de-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="651de-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="651de-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="651de-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="651de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651de-126">**Интерфейс Ивмперрор (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="651de-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="651de-127">**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="651de-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





