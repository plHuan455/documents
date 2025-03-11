### Update trong editor

```javascript
import { _decorator, CCFloat, CCString, Component, Label, Node, Prefab } from 'cc';
const { ccclass, property } = _decorator;

@ccclass('ShopItem')
export class ShopItem extends Component {
    private _health: string = "100"; // Dữ liệu kiểu string
    @property
    get health(): string {
        return this._health;
    }

    set health(value: string) {
        let num = parseInt(value); // Chuyển string thành number
        if (isNaN(num) || num < 0) {
            this._health = "0"; // Không cho phép giá trị âm hoặc không hợp lệ
        } else {
            this._health = value; // Gán giá trị hợp lệ
        }
    }
}
```
