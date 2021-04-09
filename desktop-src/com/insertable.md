---
title: Вставляемый (ключ CLSID)
description: Указывает, что объекты этого класса должны отображаться в диалоговом окне «Вставка объекта» в списке при использовании приложениями-контейнерами COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Код COM для вставляемого раздела реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071010"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="793ae-104">Вставляемый (ключ CLSID)</span><span class="sxs-lookup"><span data-stu-id="793ae-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="793ae-105">Указывает, что объекты этого класса должны отображаться в диалоговом окне « **Вставка объекта** » в списке при использовании приложениями-контейнерами com.</span><span class="sxs-lookup"><span data-stu-id="793ae-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="793ae-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="793ae-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="793ae-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="793ae-107">Remarks</span></span>

<span data-ttu-id="793ae-108">Этот ключ является обязательной записью для 32-разрядных приложений COM, объекты которых можно вставлять в существующие 16-разрядные приложения.</span><span class="sxs-lookup"><span data-stu-id="793ae-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="793ae-109">Существующие 16-разрядные приложения ищут в реестре этот раздел, который информирует приложение о том, что сервер поддерживает внедрение.</span><span class="sxs-lookup"><span data-stu-id="793ae-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="793ae-110">Если ключ для **вставки** существует, 16-разрядные приложения также могут попытаться проверить, существует ли сервер на компьютере.</span><span class="sxs-lookup"><span data-stu-id="793ae-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="793ae-111">16-разрядные приложения обычно извлекают значение ключа [**локалсервер**](localserver.md) из класса и проверяют, является ли он допустимым файлом в системе.</span><span class="sxs-lookup"><span data-stu-id="793ae-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="793ae-112">Таким образом, для 32-разрядного приложения, которое может быть вставлено 16-разрядным приложением, 32-разрядное приложение должно зарегистрировать подраздел **локалсервер** в дополнение к регистрации [**LocalServer32**](localserver32.md).</span><span class="sxs-lookup"><span data-stu-id="793ae-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="793ae-113">Эта запись, используемая с элементами управления, указывает, что объект может действовать только как внедренный объект на месте без специальных функций управления.</span><span class="sxs-lookup"><span data-stu-id="793ae-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="793ae-114">Объекты с этим ключом отображаются в диалоговом окне **Вставка объекта** для своего контейнера.</span><span class="sxs-lookup"><span data-stu-id="793ae-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="793ae-115">При использовании с элементами управления эта запись также указывает, что элемент управления был протестирован с контейнерами, не являющимися элементами управления.</span><span class="sxs-lookup"><span data-stu-id="793ae-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="793ae-116">Эта запись также является необязательной и может быть пропущена, если элемент управления не предназначен для работы с более старыми контейнерами, которые не понимают элементы управления.</span><span class="sxs-lookup"><span data-stu-id="793ae-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="793ae-117">Этот ключ отсутствует для внутренних классов, таких как классы моникера.</span><span class="sxs-lookup"><span data-stu-id="793ae-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="793ae-118">См. также</span><span class="sxs-lookup"><span data-stu-id="793ae-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




