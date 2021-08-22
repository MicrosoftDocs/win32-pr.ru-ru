---
description: Содержит входные данные для \_ команды ШАРЕДРЕСАУРЦЕ D3DAUTHENTICATEDCONFIGURE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742910"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>\_Структура КОНФИГУРЕШАРЕДРЕСАУРЦЕ D3DAUTHENTICATEDCHANNEL

Содержит входные данные для [**команды \_ шаредресаурце D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-sharedresource.md) .

Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>Члены

<dl> <dt>

**Параметры**
</dt> <dd>

[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.

</dd> <dt>

**процессидентифертипе**
</dt> <dd>

Значение [**D3DAUTHENTICATEDCHANNEL \_ процессидентифиертипе**](d3dauthenticatedchannel-processidentifiertype.md) , указывающее тип процесса. Чтобы указать процесс диспетчер окон рабочего стола (DWM), установите для этого элемента значение **процессидтипе \_ DWM**. В противном случае установите этот элемент в **процессидтипе \_ Handle** и присвойте элементу **процесшандле** допустимый маркер.

</dd> <dt>

**процесшандле**
</dt> <dd>

Обработчик процесса. Если элемент **процессидентифиер** равен процесстидтипе, то элемент **процесшандле** указывает на обработку процесса. **\_** В противном случае значение игнорируется.

</dd> <dt>

**алловакцесс**
</dt> <dd>

Если **значение — true**, указанный процесс имеет доступ к ограниченным общим ресурсам.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




