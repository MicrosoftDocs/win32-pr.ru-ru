---
title: Структура Лскэйпакк
description: Содержит сведения о конкретном пакете лицензионных ключей службы удаленных рабочих столов.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов структуры Лскэйпакк
- службы удаленных рабочих столов указателя структуры Лплскэйпакк
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8b2c7c8b6c42464e273008f9de2730b41ea64981e44583eb48f4125da3ba9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989093"
---
# <a name="lskeypack-structure"></a>Структура Лскэйпакк

Содержит сведения о конкретном пакете лицензионных ключей службы удаленных рабочих столов.

> [!Note]  
> Эта структура не определена ни в одном файле заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Версия пакета ключей.

</dd> <dt>

**уккэйпакктипе**
</dt> <dd>

Тип пакета ключей.

</dd> <dt>

**сзкомпанинаме**
</dt> <dd>

Название компании, выдавшей пакет ключей.

</dd> <dt>

**сзкэйпаккид**
</dt> <dd>

Идентификатор пакета ключей.

</dd> <dt>

**сзпродуктнаме**
</dt> <dd>

Имя продукта, которому принадлежит этот пакет ключей.

</dd> <dt>

**сзпродуктид**
</dt> <dd>

Идентификатор продукта, которому принадлежит этот пакет ключей.

</dd> <dt>

**сзпродуктдеск**
</dt> <dd>

Описание продукта, которому принадлежит этот пакет ключей.

</dd> <dt>

**вмажорверсион**
</dt> <dd>

Основной номер версии продукта, к которому относится этот пакет ключей.

</dd> <dt>

**вминорверсион**
</dt> <dd>

Дополнительный номер версии продукта, к которому относится этот пакет ключей.

</dd> <dt>

**двплатформтипе**
</dt> <dd>

Тип платформы.

</dd> <dt>

**уклиценсетипе**
</dt> <dd>

Тип лицензий в пакете ключей.

</dd> <dt>

**двлангуажеид**
</dt> <dd>

Идентификатор языка.

</dd> <dt>

**укчаннелофпурчасе**
</dt> <dd>

Канал покупки.

</dd> <dt>

**сзбегинсериалнумбер**
</dt> <dd>

Серийный номер первой лицензии.

</dd> <dt>

**двтоталлиценсеинкэйпакк**
</dt> <dd>

Общее число лицензий в пакете ключей.

</dd> <dt>

**двпродуктфлагс**
</dt> <dd>

Метки.

</dd> <dt>

**двкэйпаккид**
</dt> <dd>

Идентификатор пакета ключей.

</dd> <dt>

**уккэйпаккстатус**
</dt> <dd>

Состояние пакета ключей.

</dd> <dt>

**двактиватедате**
</dt> <dd>

Дата активации пакета ключей.

</dd> <dt>

**двекспиратиондате**
</dt> <dd>

Дата истечения срока действия пакета ключей.

</dd> <dt>

**двнумберофлиценсес**
</dt> <dd>

Число лицензий.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**тлскэйпаккенумбегин**](tlskeypackenumbegin.md)
</dt> <dt>

[**тлскэйпаккенумнекст**](tlskeypackenumnext.md)
</dt> <dt>

[**тлскэйпаккенуменд**](tlskeypackenumend.md)
</dt> </dl>

 

 





