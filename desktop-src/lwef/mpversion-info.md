---
title: Структура MPVERSION_INFO (Мпклиент. h)
description: Сведения о версии для компонентов диспетчера защиты от вредоносных программ.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO структуры устаревшие функции среды Windows
- функции PMPVERSION_INFO Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608704"
---
# <a name="mpversion_info-structure"></a>\_Структура сведений о MPVERSION

Сведения о версии для компонентов диспетчера защиты от вредоносных программ.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Продукт**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Номер версии продукта.

</dd> <dt>

**Служба**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия компонента службы.

</dd> <dt>

**филесистемфилтер**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия компонента фильтра файловой системы.

</dd> <dt>

**Ядро**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия компонента ядра.

</dd> <dt>

**ассигнатуре**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия компонента подписи антишпионского по.

</dd> <dt>

**авсигнатуре**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия компонента сигнатур Антивируса.

</dd> <dt>

**нисенгине**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия подсистемы NIS.

</dd> <dt>

**ниссигнатуре**
</dt> <dd>

Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**

</dd> <dd>

Версия компонента подписи NIS-подписи.

</dd> <dt>

**Reserved**
</dt> <dd>

Тип: **[**мпкомпонент \_ версия**](mpcomponent-version.md) \[ 4.\]**

</dd> <dd>

Зарезервированные поля.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_версия мпкомпонент**](mpcomponent-version.md)
</dt> </dl>

 

 





