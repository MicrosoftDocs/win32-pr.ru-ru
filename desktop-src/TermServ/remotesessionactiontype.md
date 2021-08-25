---
title: Перечисление Ремотесессионактионтипе
description: Используется для указания типа удаленного действия.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Ремотесессионактионтипе
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107ee44f058d776a906fef37b2e384ed6d8970224c44a6846b257c5f336c515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865714"
---
# <a name="remotesessionactiontype-enumeration"></a>Перечисление Ремотесессионактионтипе

Используется для указания типа удаленного действия.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**ремотесессионактиончармс**
</dt> <dd>

Отображает чудо в удаленном сеансе.

</dd> <dt>

<span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**ремотесессионактионаппбар**
</dt> <dd>

Отображает панель приложений в удаленном сеансе.

</dd> <dt>

<span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**ремотесессионактионснап**
</dt> <dd>

Закрепляет приложение в удаленном сеансе. Этот параметр является устаревшим и не должен использоваться.

</dd> <dt>

<span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**ремотесессионактионстартскрин**
</dt> <dd>

Приводит к отображению начального экрана в удаленном сеансе.

</dd> <dt>

<span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**ремотесессионактионаппсвитч**
</dt> <dd>

Вызывает отображение окна переключения приложения в удаленном сеансе. Это то же самое, что пользователь нажимает клавиши ALT + TAB.

</dd> <dt>

<span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**ремотесессионактионактионцентер**
</dt> <dd>

Приводит к отображению центра уведомлений в удаленном сеансе. То же самое, что пользователь нажимает клавишу Win + A.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 и Windows 8:** это значение не поддерживается до Windows Server 2016 и Windows 10.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClient8:: Сендремотеактион**](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





