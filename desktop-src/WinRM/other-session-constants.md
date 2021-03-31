---
title: Другие константы сеанса (Всмандисп. h)
description: Укажите кодировку, шифрование и порт имени субъекта-службы.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137199"
---
# <a name="other-session-constants"></a><span data-ttu-id="0d33e-103">Другие константы сеанса</span><span class="sxs-lookup"><span data-stu-id="0d33e-103">Other Session Constants</span></span>

<span data-ttu-id="0d33e-104">Константы, перечисленные в следующем списке, в перечислении **\_ \_ всмансессионфлагс** , в которых указываются кодировка, шифрование и порт имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0d33e-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="0d33e-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="0d33e-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d33e-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0d33e-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="0d33e-107">Отправляет запрос в кодировке UTF8, а не в UTF16.</span><span class="sxs-lookup"><span data-stu-id="0d33e-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="0d33e-108">Связанный метод создания скриптов — это [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) , а метод C++ — [**ивсманекс. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span><span class="sxs-lookup"><span data-stu-id="0d33e-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d33e-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**всманфлагноенкриптион**</span><span class="sxs-lookup"><span data-stu-id="0d33e-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d33e-110">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="0d33e-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="0d33e-111">Не шифровать сообщения, отправляемые по сети.</span><span class="sxs-lookup"><span data-stu-id="0d33e-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="0d33e-112">Этот параметр разрешается, только если [*прослушиватель*](windows-remote-management-glossary.md) настроен таким образом, чтобы **алловуненкриптед** было установлено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0d33e-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="0d33e-113">Связанный метод создания скриптов — это [**WSMan. сессионфлагноенкриптион**](wsman-sessionflagnoencryption.md) , а метод C++ — [**ивсманекс. сессионфлагноенкриптион**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="0d33e-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d33e-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**всманфлаженаблеспнсерверпорт**</span><span class="sxs-lookup"><span data-stu-id="0d33e-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d33e-115">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="0d33e-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="0d33e-116">Укажите порт имени субъекта-службы (SPN) при подключении непосредственно к удаленному оборудованию BMC, также известному как подключение по внешнему [*каналу*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="0d33e-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="0d33e-117">Поскольку как компьютер сервера WinRM, так и оборудование BMC могут совместно использовать один и тот же IP-адрес, этот флаг указывает на то, что для определения того, подключено ли соединение к службе или напрямую к BMC, должен использоваться номер порта SPN.</span><span class="sxs-lookup"><span data-stu-id="0d33e-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="0d33e-118">Дополнительные сведения см. в разделе [форматы имен для уникальных имен участников-служб](/windows/desktop/AD/name-formats-for-unique-spns).</span><span class="sxs-lookup"><span data-stu-id="0d33e-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="0d33e-119">Связанный метод создания скриптов — это [**WSMan. сессионфлаженаблеспнсерверпорт**](wsman-sessionflagenablespnserverport.md) , а метод C++ — [**ивсманекс. сессионфлаженаблеспнсерверпорт**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span><span class="sxs-lookup"><span data-stu-id="0d33e-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d33e-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="0d33e-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d33e-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="0d33e-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="0d33e-122">Отправляет запрос в UTF16.</span><span class="sxs-lookup"><span data-stu-id="0d33e-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d33e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0d33e-123">Requirements</span></span>



| <span data-ttu-id="0d33e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0d33e-124">Requirement</span></span> | <span data-ttu-id="0d33e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0d33e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d33e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d33e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0d33e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d33e-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0d33e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d33e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0d33e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d33e-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0d33e-130">Header</span><span class="sxs-lookup"><span data-stu-id="0d33e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d33e-131"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d33e-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d33e-132">IDL</span><span class="sxs-lookup"><span data-stu-id="0d33e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d33e-133"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d33e-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d33e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d33e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d33e-135">Константы сеанса</span><span class="sxs-lookup"><span data-stu-id="0d33e-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

