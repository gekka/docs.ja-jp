---
title: BlessIWbemServicesObject 関数 (アンマネージ API リファレンス)
description: BlessIWbemServicesObject 関数は、ユーザー資格情報が IWbemServices オブジェクトへのアクセスを許可しているかどうかを示します
ms.date: 11/06/2017
api_name:
- BlessIWbemServicesObject
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BlessIWbemServicesObject
helpviewer_keywords:
- BlessIWbemServicesObject function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94c6f47e67cf22f189719a8a9f56e830ee90227c
ms.sourcegitcommit: d2e1dfa7ef2d4e9ffae3d431cf6a4ffd9c8d378f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2019
ms.locfileid: "70798724"
---
# <a name="blessiwbemservicesobject-function"></a>BlessIWbemServicesObject 関数
ユーザー資格情報が、指定された[IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)オブジェクトへのアクセスを許可するかどうかを示します。 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>構文

```cpp
HRESULT BlessIWbemServicesObject (
   [in] IUnknown* pIUnknown,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```

## <a name="parameters"></a>パラメーター

`pIWbemServices`\
からWMI サービスオブジェクトへのポインター。

`strUser`\
からユーザー名。

`strPassword`\
からに`strUser`関連付けられているパスワード。

`strAuthority`\
からユーザーのドメイン名。 詳細については、「 [Connectserverwmi](connectserverwmi.md)関数」を参照してください。

`impLevel`\
から偽装レベル。

`authnLevel`\
から承認レベル。

## <a name="return-value"></a>戻り値

この関数によって返される次の値は、 *winerror.h*ヘッダーファイルで定義されています。また、コード内で定数として定義することもできます。

|定数  |Value  |説明  |
|---------|---------|---------|
| `E_INVALIDARG` | 0x80070057 | 1つ以上の引数が無効です。 |
| `E_POINTER` | 0x80004003 | `pIWbemServices` は `null` です。 | 
| `E_FAIL` | 0x80000008 | 特定できないエラーが発生しました。 |
| `E_OUTOFMEMORY` | 0x80000002 | 操作を実行するのに十分なメモリがありません。 | 
| `S_OK` | 0 | 関数の呼び出しに成功しました。 | 

## <a name="requirements"></a>必要条件

 **・** [システム要件](../../get-started/system-requirements.md)に関するページを参照してください。

 **ヘッダー:** WMINet_Utils

 **.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>関連項目

- [WMI およびパフォーマンスカウンター (アンマネージ API リファレンス)](index.md)
