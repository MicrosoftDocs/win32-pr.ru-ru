---
description: Представляет сведения о соединении с принтером.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Структура PRINTER_CONNECTION_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814865"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="2142c-103">\_ \_ Структура 1. сведения о подключении принтера \_</span><span class="sxs-lookup"><span data-stu-id="2142c-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="2142c-104">Представляет сведения о соединении с принтером.</span><span class="sxs-lookup"><span data-stu-id="2142c-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2142c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2142c-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="2142c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="2142c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2142c-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="2142c-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2142c-108">Определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2142c-108">The following values are defined:</span></span>



| <span data-ttu-id="2142c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="2142c-109">Value</span></span>                                      | <span data-ttu-id="2142c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2142c-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2142c-111">\_Несоответствие подключения к принтеру \_ (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="2142c-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="2142c-112">Если этот флаг bit установлен, подключение принтера не соответствует.</span><span class="sxs-lookup"><span data-stu-id="2142c-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="2142c-113">Пользователь может предоставить локальный драйвер печати как *псздривернаме* и использовать его для подготовки к просмотру вместо использования драйвера, установленного на принтере сервера, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="2142c-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="2142c-114">\_Подключение принтера \_ без \_ пользовательского интерфейса (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="2142c-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="2142c-115">Если этот флаг bit установлен, то этот вызов не может отобразить диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2142c-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="2142c-116">Если необходимо отобразить диалоговое окно для установки драйвера принтера с сервера, а этот флаг установлен, то драйвер принтера не будет установлен, подключение принтера не будет добавлено, и вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2142c-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="2142c-117">**Windows 7:** В Windows 7 и более поздних версиях Windows если этот флаг установлен и пользователь работает в режиме с повышенными правами, диалоговое окно " **доверять этому принтеру** " не отображается.</span><span class="sxs-lookup"><span data-stu-id="2142c-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2142c-118">**псздривернаме**</span><span class="sxs-lookup"><span data-stu-id="2142c-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="2142c-119">Указатель на имя драйвера.</span><span class="sxs-lookup"><span data-stu-id="2142c-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2142c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2142c-120">Requirements</span></span>



| <span data-ttu-id="2142c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2142c-121">Requirement</span></span> | <span data-ttu-id="2142c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2142c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2142c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2142c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2142c-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2142c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2142c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2142c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2142c-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2142c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2142c-127">Header</span><span class="sxs-lookup"><span data-stu-id="2142c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2142c-128"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2142c-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2142c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2142c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2142c-130">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="2142c-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2142c-131">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="2142c-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




