---
title: Привязка данных
description: Привязка данных
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700945"
---
# <a name="databinding"></a><span data-ttu-id="26d4b-103">Привязка данных</span><span class="sxs-lookup"><span data-stu-id="26d4b-103">Databinding</span></span>

<span data-ttu-id="26d4b-104">Добавлен новый атрибут DataBinding, позволяющий свойствам различать взаимодействующие изменения, только когда фокус оставляет за собой элемент управления или во время всех уведомлений об изменении свойств.</span><span class="sxs-lookup"><span data-stu-id="26d4b-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="26d4b-105">Новый атрибут, известный как Иммедиатебинд, позволяет элементам управления различать два разных типа связываемых свойств.</span><span class="sxs-lookup"><span data-stu-id="26d4b-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="26d4b-106">Один тип связываемого свойства должен уведомлять каждое изменение базы данных, например, с элементом управления "флажок", в котором каждое изменение необходимо отправить в основную базу данных, даже если элемент управления не потерял фокус.</span><span class="sxs-lookup"><span data-stu-id="26d4b-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="26d4b-107">Однако для таких элементов управления, как ListBox, требуется, чтобы изменение свойства было уведомлено к базе данных, когда элемент управления теряет фокус, так как пользователь мог изменить выделенный фрагмент с помощью клавиш со стрелками перед настройкой нужного параметра, чтобы уведомление об изменении отправлялось в базу данных при каждом нажатии пользователем клавиши со стрелкой, вы получите неприемлемую производительность.</span><span class="sxs-lookup"><span data-stu-id="26d4b-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="26d4b-108">Новое свойство немедленной привязки позволяет отдельным связываемым свойствам в форме задать такое поведение, если этот бит задан, и все изменения будут уведомлены.</span><span class="sxs-lookup"><span data-stu-id="26d4b-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="26d4b-109">Новый бит Иммедиатебинд сопоставляется с новыми ВАРФЛАГ \_ фиммедиатебинд (0x80) и функфлаг \_ фиммедиатебинд (0x80) в перечислениях ВАРФЛАГС и функфлагс для интерфейса [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , который позволяет проверять атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="26d4b-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 