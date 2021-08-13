---
description: 'виатрансферпарамс передается в приложение во время передачи данных системой времени выполнения Windowsного образа (WIA) в метод ивиатрансферкаллбакк:: трансферкаллбакк.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Структура Виатрансферпарамс (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 7d128a39ff5d9d29bf0766273adaace7eae86b10c9556284c1f5b6f1c9285d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449913"
---
# <a name="wiatransferparams-structure"></a>Структура Виатрансферпарамс

**виатрансферпарамс** передается в приложение во время передачи данных системой времени выполнения Windowsного образа (WIA) в метод [**ивиатрансферкаллбакк:: трансферкаллбакк**](-wia-iwiatransfercallback-transfercallback.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>Члены

<dl> <dt>

**лмессаже**
</dt> <dd>

Тип: **Long**

</dd> <dd>

Указывает состояние передаваемых данных.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_состояние сообщений \_ \_ о переносе WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ конец \_ \_ потока сообщения передачи WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ конец \_ \_ перемещения сообщения о переносе WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_ \_ \_ состояние устройства сообщения \_ о перепереносе WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ Новая страница сообщения о переносе WIA \_**


</dt> <dd></dd> </dl> </dd> <dt>

**лперценткомплете**
</dt> <dd>

Тип: **Long**

</dd> <dd>

Указывает ход выполнения операции перемещения данных в процентах.

</dd> <dt>

**ултрансферредбитес**
</dt> <dd>

Тип: **ULONG64**

</dd> <dd>

Указывает объем передаваемых данных.

</dd> <dt>

**хреррорстатус**
</dt> <dd>

Тип: **HRESULT**

</dd> <dd>

Состояние (или состояние ошибки) устройства, установленного драйвером; Например, "прогрев".

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                   |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




