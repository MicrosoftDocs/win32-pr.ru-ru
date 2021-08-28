---
title: DXCoreNotificationType
description: Определяет константы, указывающие типы уведомлений, создаваемых объектами [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) или [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) .
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 230b6c103f83e72dfe0ba7803cde4b4695a32de724ce44c1aaccf5131d077bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726014"
---
# <a name="dxcorenotificationtype-enum"></a>Перечисление Дкскоренотификатионтипе

Определяет константы, указывающие типы уведомлений, создаваемых объектами [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) или [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) .

Вы можете зарегистрировать эти уведомления и отменить их регистрацию, вызвав [идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) и [Идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)соответственно.

## <a name="syntax"></a>Синтаксис

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Константы

### <a name="adapterliststale"></a>адаптерлистстале

Это уведомление создается объектом <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">идкскореадаптерлист</a> , когда список адаптеров становится устаревшим. Новый переход является односторонним и одноразовым, поэтому это уведомление создается не чаще одного раза.

### <a name="adapternolongervalid"></a>адаптернолонжервалид

Это уведомление создается объектом <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">идкскореадаптер</a> , когда адаптер становится недействительным. Переход "действительно-к-недопустим" является односторонним и одноразовым, поэтому это уведомление создается не чаще одного раза.

### <a name="adapterbudgetchange"></a>адаптербуджетчанже

Это уведомление создается объектом <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">идкскореадаптер</a> , когда происходит изменение бюджета адаптера. Это уведомление может происходить много раз. Использование этого уведомления функционально похоже на <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3:: регистервидеомеморибуджетчанженотификатионевент</a>. В ответ на это событие необходимо вызвать метод [идкскореадаптер:: куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md) (с [Дкскореадаптерстате:: адаптермеморибуджет](./ne-dxcore_interface-dxcoreadapterstate.md)) для вычисления текущего состояния бюджета памяти.

### <a name="adapterhardwarecontentprotectionteardown"></a>адаптерхардвареконтентпротектионтеардовн

Это уведомление создается объектом <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">идкскореадаптер</a> для уведомления об уничтожении защиты аппаратного содержимого адаптера. Это уведомление может происходить много раз. Он функционально похож на <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3:: регистерхардвареконтентпротектионтеардовнстатусевент</a>. В ответ на это событие следует повторно оценить текущее состояние сеанса шифрования; Например, путем вызова [ID3D11VideoContext1:: чекккриптосессионстатус](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) , чтобы определить влияние аппаратного уничтожения на определенный интерфейс [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) .

## <a name="see-also"></a>См. также

[Идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [Идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Использование DXCore для перечисления адаптеров](../dxcore-enum-adapters.md)